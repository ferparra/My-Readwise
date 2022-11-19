title:: Database Thread Alert: S... (highlights)
author:: [[@narayanarjun on Twitter]]
full-title:: "Database Thread Alert: S..."
category:: #tweets
url:: https://twitter.com/narayanarjun/status/1128393193941274624

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- DATABASE THREAD ALERT: So @memsql ran some database benchmarks and threw some shade at @CockroachDB. As super serious professionals with a serious company name, I imagine the Roach is going to be measured in their response. As an UNSHACKLED database enthusiast I am... not. ([View Tweet](https://twitter.com/narayanarjun/status/1128393193941274624))
		- **Note**: Thread
	- >> BEGIN RANT;
	  Let's focus on TPC-C to start. First, they have some bar graphs with loooooong bars for MemSQL, and short stubby bars for CockroachDB. Wow, such performance. Very impress. ([View Tweet](https://twitter.com/narayanarjun/status/1128393194822164480))
	- The problem is that TPC-C has a strict limit on how many transactions you're allowed to run (the "tpmC) per 'scalefactor'. The goal is to prevent you from running 10000 transactions on a mere 10 megs of data (Look ma, no L2 cache misses!). MemSQL does not obey this limit. ([View Tweet](https://twitter.com/narayanarjun/status/1128393195866460161))
	- The benchmark goal is to force you to 'scale out' your data if you want to show bigger numbers. Roughly, it's 12.8 tpmC per warehouse (which is about 80 megs of unreplicated state). Want to show 100,000 tpmC? Gotta have a working set of 600 gigabytes of data (times replication!). ([View Tweet](https://twitter.com/narayanarjun/status/1128393196705386496))
	- MemSQL, instead, shows 800,000 tpmC on scale factor 10,000. This is not allowed. At SF 10,000, you're limited to ~128,000 tpmC. The point is this: if you want to show more tpmC, do it at higher data scalefactors.
	  But MemSQL says they didn't cheat, so what gives? ([View Tweet](https://twitter.com/narayanarjun/status/1128393197451976704))
	- OK, so forget the ridiculously long bars that are completely off-spec. Instead, let's talk about why you put things in a database in the first place. Probably cause you like the data and you'd like to keep it around. So how does this little detail look to you? 
	  
	  ![](https://pbs.twimg.com/media/D6jDyWWXsAAvST1.png) ([View Tweet](https://twitter.com/narayanarjun/status/1128393198219427840))
	- @MemSQL made actually keeping the data around purely optional. I don't know about your experience with computers, but if you make the fsync part optional, this tends to end pretty badly. I dunno how else to put this, but this seems... pretty Mongo. ([View Tweet](https://twitter.com/narayanarjun/status/1128393199943344129))
	- "But Arjun, they use synchronous replication! Isn't that sufficient?" I can imagine the retort. No. Because neither machine is required to write it down, and they don't replicate across datacenters (MemSQL only supports async cross-DC replication[1]).
	  [1] https://t.co/7R9uCGUjMs ([View Tweet](https://twitter.com/narayanarjun/status/1128393200857751553))
	- So you're necessarily in a single AZ deployment (MemSQL is incapable of HA across clusters), and nobody is writing anything to durable storage. I hope this data isn't important to you. Probably not right, I mean, you're only transacting with it thousands of times a second... ([View Tweet](https://twitter.com/narayanarjun/status/1128393201746874368))
	- Enough dunking on their TPC-C. On to TPC-H. This is the legacy data warehouse benchmark. It really tests your ability to do SQL query optimization, and you really need a columnar in-memory representation to squeeze the juice out of these queries. MemSQL does decently here, kudos! ([View Tweet](https://twitter.com/narayanarjun/status/1128393202489266177))
	- But TPC-H is a bit of a legacy benchmark, known to be deceptively easy to optimize, because the data is simply not realistic enough[1]. TPC-DS is much better! And on that benchmark, MemSQL is beaten by ~2x perf by an unnamed 'Cloud DW' product.
	  
	  [1] https://t.co/c0m3iN8RhU ([View Tweet](https://twitter.com/narayanarjun/status/1128393203273687040))
	- But wait... what's the Y axis on their graph? "Sum of Query Runtimes"? According to MemSQL, they only report a 'power run' number. 
	  
	  ![](https://pbs.twimg.com/media/D6jXxh4WAAIme5D.png) ([View Tweet](https://twitter.com/narayanarjun/status/1128393204305362944))
	- Let's see what the TPC-DS spec has to say about the proper way to compare performance... 
	  
	  ![](https://pbs.twimg.com/media/D6jaPmqXoAADmaq.jpg) ([View Tweet](https://twitter.com/narayanarjun/status/1128393206557814784))
	- Hm, sure seems to be a lot more complicated! Let's head over to the 'The Making of TPC-DS' paper[1] to see what they have to say about power runs... Hmm.
	  
	  [1] https://t.co/rPXLxTb3ex 
	  
	  ![](https://pbs.twimg.com/media/D6jaJaaXsAAHva2.jpg) ([View Tweet](https://twitter.com/narayanarjun/status/1128393208923398147))
	- Listen, I get that benchmarking is really, really, hard. Which is why it's best approached with humility, and serious methodological rigor.
	  
	  But if you're gonna throw cheap shade, you best not miss.
	  >> COMMIT RANT https://t.co/VvcKhuWxMh ([View Tweet](https://twitter.com/narayanarjun/status/1128393210701676547))
	- UPDATE: Kudos to MemSQL for removing the comparison. Unlike the original snarky post and my ultra-snarky response, they've handled the follow-up with grace and humility and we should applaud them for it!
	  https://t.co/FmsRQUwz7S ([View Tweet](https://twitter.com/narayanarjun/status/1129171608088842240))