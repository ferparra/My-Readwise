title:: `A = 0-X`  Is About 3-10... (highlights)
author:: [[@mhevery on Twitter]]
full-title:: "`A = 0-X`  Is About 3-10..."
category:: #tweets
url:: https://twitter.com/mhevery/status/1626002464469323777

- Highlights first synced by [[Readwise]] [[Feb 16th, 2023]]
	- `a = 0-x`  is about 3-10x faster than `a = -x`  🤯
	  
	  Let's jump into JavaScript VM details to see why and how to guard against this VM de-opt:
	  
	  🧵🪡🧶 
	  
	  ![](https://pbs.twimg.com/media/FpC4nq5aUAI5t8H.jpg) ([View Tweet](https://twitter.com/mhevery/status/1626002464469323777))
		- **Note**: Thread
	- The first thing to understand is that JavaScript has two representations for numbers:
	- Let's assume: `x` is an Integer and `x = 0`
	  `0-x` => `0-0 => 0`, Result is `0` (Integer) Perfect!
	  `-x` => negate `x`.
	- Why is this a de-opt:
	  
	  1) Array access requires an Integer. So VM has to guard for Floats and convert Float (-0) into Integer(0);
	  
	  2) VMs have special "fast" arrays for all integers but use a more generic (slower) array for an array of mixed types (such as Integers and Floats) 
	  
	  ![](https://pbs.twimg.com/media/FpC4pqqaIAAL8nh.jpg) ([View Tweet](https://twitter.com/mhevery/status/1626002500393529344))
	- Different browsers have different perf penalties for this, but my tests show a 3-10x slow down on Apple M1:
	  
	  Try it yourself: https://t.co/LJH3Phg4o2 
	  
	  ![](https://pbs.twimg.com/media/FpC4qa9aAAAWyYw.jpg) ([View Tweet](https://twitter.com/mhevery/status/1626002513270042624))
	- Learnings: