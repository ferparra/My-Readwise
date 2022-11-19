title:: Concurrent Programming C... (highlights)
author:: [[@rsms on Twitter]]
full-title:: "Concurrent Programming C..."
category:: #tweets
url:: https://twitter.com/rsms/status/1407836523555217408

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Concurrent programming can be hard. After days (over the course of weeks) I was today finally able to make a channel implementation pass my tests. Sometimes the smallest things takes the most time to get right.
	  
	  Here's a short thread … https://t.co/xBubJLuQdt ([View Tweet](https://twitter.com/rsms/status/1407825026162651136))
		- **Note**: Thread
	- The kind of "channel" I've implemented is a form of CSP (see https://t.co/G1kkK4GAkz) which is used to communicate between threads. It's similar to Go's chan but works with threads rather than a custom coroutine runtime. ([View Tweet](https://twitter.com/rsms/status/1407825180404031490))
	- (Image from https://t.co/NdzVbgrF3I) 
	  
	  ![](https://pbs.twimg.com/media/E4maPL-VUAEbizy.png) ([View Tweet](https://twitter.com/rsms/status/1407825970220969984))
	- There are just two operations: send and receive.
	  send() blocks until there's a thread calling recv()
	  recv() blocks until there's a thread calling send()
	  A channel may be buffered in which case send and recv may succeed immediately.
	  So what makes this so challenging? ([View Tweet](https://twitter.com/rsms/status/1407826039951171584))
	- Time and causality; avoiding deadlocks and carefully handling CPU cache hierarchies, all while being efficient in time and space. For this to not be a confusing wild goose chase of trial and error, we need to have Mechanical Sympathy. ([View Tweet](https://twitter.com/rsms/status/1407826085102850050))
	- "Mechanical Sympathy" is a term coined by racing driver Jackie Stewart. Paraphrased and applied to computers: "You don’t have to be a hardware engineer to write good software, but you do have to have Mechanical Sympathy". What this means to me … ([View Tweet](https://twitter.com/rsms/status/1407826173506162689))
	- What this means to me is that having a sense of how the computer works helps tremendously in writing correct, efficient and elegant software, even if I don't fully understand all the details of the hardware. ([View Tweet](https://twitter.com/rsms/status/1407826206284607489))
	- One of the key aspects of modern software performance is managing memory. Modern CPUs have a hierarchy of data caches in addition to main working memory (RAM.) CPUs today can complete a staggering amount of computations through not just raw clock speed but … 
	  
	  ![](https://pbs.twimg.com/media/E4mal6xVUAUZWxC.png) ([View Tweet](https://twitter.com/rsms/status/1407826369644355591))
	- … through a complex combination of clever "temporal" tricks, like intra-core pipeline parallelism and predicting what will be needed soon — the latter is key and involves the CPU and its cores moving instructions and data around in the various caches … ([View Tweet](https://twitter.com/rsms/status/1407826485721763849))
	- … (aka "line caches.") To write fast software you need to "trick" the CPU into invalidating as little data in its caches as possible. Each cache level is usually several orders of magnitude faster than the next. Don't be surprised by a 400x performance difference. ([View Tweet](https://twitter.com/rsms/status/1407826560816582658))
	- A second important fallout of this kind of hardware design is that changes to data done by one core may note be visible to another core at the same point in time. A simple example is a counter: Without some form of synchronization the value will become corrupt. 
	  
	  ![](https://pbs.twimg.com/media/E4mcWQTUcAEnwme.png) ([View Tweet](https://twitter.com/rsms/status/1407828476204228615))
	- We'd expect the counter x in the image to be 2 after it has been incremented twice, but it's 1!
	  Shared memory is simply a hard problem to solve efficiently. What we need to do is to tell the CPU that "x may be modified by other cores" causing loads & stores to shared memory. ([View Tweet](https://twitter.com/rsms/status/1407829105362407424))
	- But that's really slow, as discussed earlier. So a better implementation of a multi-process counter is to give each core it's own counter and then occasionally as them to store their results to shared memory and ask one of them to sum up all counters. 
	  
	  ![](https://pbs.twimg.com/media/E4merb-VcAIoI4O.png) ([View Tweet](https://twitter.com/rsms/status/1407830844908048388))
	- This is better and will be faster than a naïve "locking"/"synchronized" counter (if we ignore the up-front costs of introducing multithreading in the first place.) But we might run into another problem here which affects performance and correctness in some cases: false sharing. ([View Tweet](https://twitter.com/rsms/status/1407831361977683971))
	- "False sharing" is seemingly weird term for what happens when multiple cores update memory that sits inside the same "cache line". Chances are your CPU's cache line size is 64 bytes and that it chunks up memory into cache lines by simply aligning addresses to 64. ([View Tweet](https://twitter.com/rsms/status/1407832198095380481))
	- (Image from https://t.co/pLFBVtXN7S) 
	  
	  ![](https://pbs.twimg.com/media/E4mgUAXVoAErQ6R.png) ([View Tweet](https://twitter.com/rsms/status/1407832635754250243))
	- So for our parallel counter example we need to make sure that the memory of the core-specific counters x¹ and x² lie inside separate cache line boundaries. This is easy to do in C et al. If you look at MP-forward code like Intel TBB or LMAX Disruptor you'll see this a lot. 
	  
	  ![](https://pbs.twimg.com/media/E4mhuPyVcAUQ51y.jpg) ([View Tweet](https://twitter.com/rsms/status/1407834262691139584))
	- Okay that's going to make our silly parallel counter really efficient.
	  
	  So what's up with this channel thing I've been struggling with?
	  
	  Well, I wanted to make it very fast and avoid thread sync. TLDR: I reached a compromise.
	  
	  How many implementation attempts did I make? Many: 
	  
	  ![](https://pbs.twimg.com/media/E4migjWVkAUw2em.png) ([View Tweet](https://twitter.com/rsms/status/1407835045398646785))
	- After researching and testing existing solutions, I tried to port a few of them. One neat one is Plan 9's libthread but that one, like the Go implementation, relies on a coroutine runtime but could be adopted to work with plain C11 threads. ([View Tweet](https://twitter.com/rsms/status/1407835511780040705))
	- I also tried porting a few other approaches like the (very java, very complex lol) LMAX Disruptor (which sadly requires call-site level changes so that went out the door) and Intel TBB's concurrent_queue which was an exercise in unwrapping 100 layers of complex C++ to … ([View Tweet](https://twitter.com/rsms/status/1407835948080013312))
	- … understand it. So that was fun. The TBB implementation was actually a pretty good fit, but I must have made some mistake as after 20 hours of debugging a correctness issue I have up. Also, the code was too complex (my C port was 1000 lines, C++ original is like 10x that.) ([View Tweet](https://twitter.com/rsms/status/1407836523555217408))