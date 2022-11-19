title:: A Few Takes on How Hardc... (highlights)
author:: [[@vkostyukov on Twitter]]
full-title:: "A Few Takes on How Hardc..."
category:: #tweets
url:: https://twitter.com/vkostyukov/status/1523055814298062848

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- A few takes on how hardcore @TwitterEng has been. Let's talk about @finagle and Scala for a minute. ([View Tweet](https://twitter.com/vkostyukov/status/1523055814298062848))
		- **Note**: Thread
	- I'd say it's pretty hardcore to adopt Scala 2.7 in 2009, when about +-0 people used it in production. Well, Twitter Eng did just that. Made a pretty big bet that worked out pretty well.
	  
	  https://t.co/CzgmNzqa4u ([View Tweet](https://twitter.com/vkostyukov/status/1523055815543824385))
	- IMO it's hardcore to implement your own Futures that Scala Futures still didn't catch up to. Twitter Futures were way ahead of their time with cancelations, locals, and root compression (think infinite Future recursion that is stack-safe and memory-leak-proof). ([View Tweet](https://twitter.com/vkostyukov/status/1523055817456447488))
	- Would you say that implementing your own network protocols is hardcore? I'd say so. Twitter Eng designed and built Mux, a multiplexing and lightweight protocol for @finagle that predates the final release of HTTP/2 by a few years. In our benchmarks, it's still 2x faster than H2. ([View Tweet](https://twitter.com/vkostyukov/status/1523055818614054912))
	- Now back to Futures and Mux. Do you think it's hardcore saying rpcFuture.cancel() and expecting your RPC middleware to propagate that over the wire? I think it is and @finagle has been doing it for a decade. ([View Tweet](https://twitter.com/vkostyukov/status/1523055819708715008))
	- Future Locals are pretty hardcore too, IMO. Think of  RPC context (eg, trace id) that is carefully threaded through your flatMaps (async boundaries) and RPC calls (network boundaries) without you (a developer) lifting a finger. ([View Tweet](https://twitter.com/vkostyukov/status/1523055820879015936))
	- Do you know what else is hardcore? @finagle's load balancer that's with very minimal coordination implements subsetting w/o load banding.
	  
	  https://t.co/rKk59Vd6Fz ([View Tweet](https://twitter.com/vkostyukov/status/1523055822015660032))
	- Finagle has the most hardcore load shedding machinery that's so simple you can write its code on a sticky note. We call it Offload AC and we've seen it push some production services' CPU utilization north of 95% without major latency degradation. ([View Tweet](https://twitter.com/vkostyukov/status/1523055823194247169))
	- I think being an extensible library is also pretty hardcore. Finagle is so generic in its concepts that we reuse a big chunk of middleware between 8 or so protocols that it implements. ([View Tweet](https://twitter.com/vkostyukov/status/1523055824330891265))
	- The core framework is so powerful and composable that our own finagle-grpc (not yet OSSed) implementation is probably <1000 LOC. ([View Tweet](https://twitter.com/vkostyukov/status/1523055825433948161))
	- In my opinion "freedom to innovate" = hardcore and by that definition @finagle has been the most hardcore RPC framework that I know of. It may as well be the only somewhat FP-flavored runtime used at such scale. ([View Tweet](https://twitter.com/vkostyukov/status/1523113041612591104))