title:: Having a Lot of Fun With... (highlights)
author:: [[@plasticine on Twitter]]
full-title:: "Having a Lot of Fun With..."
category:: #tweets
url:: https://twitter.com/plasticine/status/1391628241463480320

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- Having a lot of fun with a little Skunk Works project for @up_banking that I’m rather excited about lately! 👨‍🔬 Android UI testing is a really tough problem space, & our current setup has been pretty painful for a while—with CI duration & flakiness being a growing frustration. 🥲 ([View Tweet](https://twitter.com/plasticine/status/1391628234429648901))
		- **Note**: Thread
	- Turns out that hardware acceleration is (surprise, surprise) rather important to get emulation working well, and I’ve managed to get a pretty nice little setup going on top of our existing autoscaling @buildkite cluster sitting on top of geodistributed @GoogleCloudTech instances. ([View Tweet](https://twitter.com/plasticine/status/1391628236891643905))
	- With a few tweaks to ensure that KVM is being properly used, and the ability to attach GPUs on these GCP instances we can then pass them through to QEMU to run the emulator process, and see some pretty incredible increases in throughput & stability from initial testing. ([View Tweet](https://twitter.com/plasticine/status/1391628239227916289))
	- Boot times go from 120s → 18s, the CPU is now not bound up doing GPU work (this is huge)—even through VNC you can perform gestures perfectly, & the whole thing runs like 🧈 at 60fps! Still early days but pretty excited for what this is going to mean for our native pipeline! 🚀 ([View Tweet](https://twitter.com/plasticine/status/1391628241463480320))