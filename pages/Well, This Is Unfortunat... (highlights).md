title:: Well, This Is Unfortunat... (highlights)
author:: [[@marcan42 on Twitter]]
full-title:: "Well, This Is Unfortunat..."
category:: #tweets
url:: https://twitter.com/marcan42/status/1494213855387734019

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Well, this is unfortunate. It turns out Apple's custom NVMe drives are amazingly fast - if you don't care about data integrity.
	  
	  If you do, they drop down to HDD performance. Thread. ([View Tweet](https://twitter.com/marcan42/status/1494213855387734019))
		- **Note**: Thread
	- For a while, we've noticed that random write performance with fsync (data integrity) on Asahi Linux (and also on Linux on T2 Macs) was terrible. As in 46 IOPS terrible. That's slower than many modern HDDs.
	  
	  We thought we were missing something, since this didn't happen on macOS. ([View Tweet](https://twitter.com/marcan42/status/1494213859594616834))
	- As it turns out, macOS cheats. On Linux, fsync() will both flush writes to the drive, and ask it to flush its write cache to stable storage.
	  
	  But on macOS, fsync() only flushes writes to the drive. Instead, they provide an F_FULLSYNC operation to do what fsync() does on Linux. ([View Tweet](https://twitter.com/marcan42/status/1494213862970707969))
	- So effectively macOS cheats on benchmarks; fio on macOS does not give numbers comparable to Linux, and databases and other applications requiring data integrity on macOS need to special case it and use F_FULLSYNC.
	  
	  How bad is it if you use F_FULLSYNC? It's bad. ([View Tweet](https://twitter.com/marcan42/status/1494213865613426688))
	- Single threaded, simple Python file rewrite test:
	  
	  Macbook Air M1 (macOS):
	- So, effectively, Apple's drive is faster than all the others without cache flushes, but it is more than 3 times slower than a lowly SATA SSD at flushing its cache. Even if all you wrote is a couple of sectors. You pay a huge flush penalty if you do *any* writes. ([View Tweet](https://twitter.com/marcan42/status/1494213871149940737))
	- Here, "flushing" on macOS means F_FULLSYNC and "not" means fsync(); on Linux both are fsync(), but "not flushing" is measured by telling Linux that the drive write cache is write-through (which stops it from issuing cache flushes). ([View Tweet](https://twitter.com/marcan42/status/1494213873993682946))
	- Note that the numbers are filesystem-dependent (and encryption makes things more complicated); e.g. the SATA SSD numbers double on VFAT vs. my root filesystem (ext4 on LVM on dm-crypt), but the pattern is clear. ([View Tweet](https://twitter.com/marcan42/status/1494213876657049600))
	- macOS doesn't even seem to try to proactively issue syncs; you can write a file on macOS, fsync() it, wait 5 seconds, issue a hard reboot (e.g. via USB-PD command), and the data is gone. That's pretty bad. ([View Tweet](https://twitter.com/marcan42/status/1494213879089737729))
	- Of course, in normal usage, this is basically never an issue on laptops; given the right software hooks, they should never run out of power before the OS has a chance to issue a disk flush command. But it certainly is for desktops. And it's a bit fragile re: panics and such. ([View Tweet](https://twitter.com/marcan42/status/1494213881509875712))
	- Unfortunately, this manifests itself as quite visible issues on Linux. For example, apt-get on Asahi Linux is noticeably slow. Making fsync() not really flush on macOS is not fair; lots of portable software is written to assume fsync() means your data is safe. ([View Tweet](https://twitter.com/marcan42/status/1494213883976101888))
	- Our current thinking is we're going to add a knob to the NVMe driver to defer flush requests up to a maximum time of e.g. 1 second. That would ensure that a hard shutdown never loses you more than 1 second of data, which is better than what macOS can claim right now. ([View Tweet](https://twitter.com/marcan42/status/1494213886928908288))
	- Alas, that's still not quite safe. Not flushing means we cannot guarantee ordering of writes, which means you could end up with actual data corruption in e.g. a database, not just data loss. There's no good way around this other than doing full flushes. ([View Tweet](https://twitter.com/marcan42/status/1494213889646796802))
	- So the unfortunate conclusion is that if you're e.g. running a transactional database on Apple hardware, and you need to be able to survive a hard poweroff without data corruption, you're never going to get more than ~46 TPS.
	  
	  Unless Apple improves their ANS firmware to fix this. ([View Tweet](https://twitter.com/marcan42/status/1494213892331163649))
	- And for what it's worth, I inadvertently triggered a data consistency issue in macOS while testing this. Before running any tests I had GarageBand open. I closed it without saving the open project. After the first hard reboot later, it tried to reopen it and threw up an error. ([View Tweet](https://twitter.com/marcan42/status/1494215160218939392))
	- So I guess the unsaved project file got (partially?) deleted, but not the state that tells it to reopen the currently open file on startup.
	  
	  Data consistency matters. ([View Tweet](https://twitter.com/marcan42/status/1494215321125007362))
	- Update: tested on the Mac Mini by pulling the plug (which is a "normal" case; the USB-PD thing was a bit special). Still lost seconds of fsync()ed data. There is no (working) last-gasp flush mechanism. ([View Tweet](https://twitter.com/marcan42/status/1494221053220257795))
	- Further testing: doing this on FAT32 (to avoid APFS write amplification, which is a separate problem...) doesn't help with the IOPS on flush, but then I can look at powermetrics bandwidth stats to see what NVMe is doing. ([View Tweet](https://twitter.com/marcan42/status/1494255642202484743))
	- Artificially throttled ~30 IOPS without full cache flushes, I get 93.52 ops/s 397.77 KBytes/s disk IO, which is reasonable, and:
	  
	  ANS2 RD                         : 0.328 MB/s
	  ANS2 WR                         : 0.399 MB/s
	  
	  That's NVMe controller DRAM bandwidth. Reasonable. ([View Tweet](https://twitter.com/marcan42/status/1494255645612474369))
	- But doing flushes, this jumps to:
	  
	  ANS2 RD                         : 6.248 MB/s
	  ANS2 WR                         : 9.909 MB/s
	  
	  So that NVMe controller is doing *something* memory-intensive on flush commands. Maybe it does a linear scan over a large cache hashtable? ([View Tweet](https://twitter.com/marcan42/status/1494255649026625537))
	- I can get these stats because the NVMe controller is integrated into the SoC and "drive cache" is just normal memory (it's unified just like GPU memory), and Apple have very good instrumentation of things like DRAM bandwidth utilization from different SoC agents. ([View Tweet](https://twitter.com/marcan42/status/1494256049150640129))
	- Uh, guys? I'm not saying "the machines are only fast because they cheat on data durability". I'm saying there's a stupid, unfortunate performance bug when you *do* want durability that most people won't notice because macOS gives you poor durability by default. ([View Tweet](https://twitter.com/marcan42/status/1494293060020506626))
	- These SSDs are still fast for many use cases, and on laptops you don't care about this issue because there's a battery backup anyway.
	  
	  And besides, Apple can almost certainly fix this in a firmware upgrade. ([View Tweet](https://twitter.com/marcan42/status/1494293064579686400))
	- Chances are this happened because this design came from iDevices, where there's always a battery, so software will never hit drive cache related consistency/durability issues, so probably ~no iOS software ever uses a full sync, so nobody noticed it's slow. ([View Tweet](https://twitter.com/marcan42/status/1494293067771564040))
	- And I'm just the Nth guy to facepalm when I found out that macOS makes data durability double-opt-in with a nonstandard request. That's dumb, but it has nothing to do with the machines. It's just the reason why fio was magically fast on macOS and not on Linux. ([View Tweet](https://twitter.com/marcan42/status/1494293071118614529))
	- Note that the NVMe controller behaves in a perfectly spec-compliant way as far as data durability. It's just (ridiculously) slow when you ask for it. Probably a bug. ([View Tweet](https://twitter.com/marcan42/status/1494293769134690305))
	- But since incessant people on HN made me do another test, and for giggles:
	  
	  FAT32 on internal NVMe with F_FULLFSYNC: 58 IOPS
	  FAT32 on a cheapo USB3 flash drive with the same: 223 IOPS.
	  
	  If you run a durable database on an M1 today, try a cheap flash drive. It'll be faster :-) ([View Tweet](https://twitter.com/marcan42/status/1494307439906533376))
	- Of course, the flash drive doesn't have a cache at all, so it remains at 223 IOPS with fsync() vs. 60000 IOPS or so on NVMe - so make sure you go with NVMe if you're on a laptop where it's safe, only use the cheapo drive on Mac Minis and iMacs! 😇 ([View Tweet](https://twitter.com/marcan42/status/1494307794182631424))