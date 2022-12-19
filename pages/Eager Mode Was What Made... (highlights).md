title:: Eager Mode Was What Made... (highlights)
author:: [[@cHHillee on Twitter]]
full-title:: "Eager Mode Was What Made..."
category:: #tweets
url:: https://twitter.com/cHHillee/status/1601371638913638402

- Highlights first synced by [[Readwise]] [[Dec 10th, 2022]]
	- Eager mode was what made PyTorch successful. So why did we feel the need to depart from eager mode in PyTorch 2.0?
	  
	  Answer: it's the damn hardware! 
	  
	  Let's tell a story about how the assumptions PyTorch were based off of became untrue, and why PyTorch needed to evolve. (1/10) ([View Tweet](https://twitter.com/cHHillee/status/1601371638913638402))
		- **Note**: Thread
	- When PyTorch first came out, the prevailing wisdom was that eager-mode sacrificed performance for more flexibility.
	  
	  But in practice, people didn't really notice performance gaps! In fact, in many cases, people found PyTorch to be *faster* than graph-mode frameworks.
	  
	  Why? (2/10) ([View Tweet](https://twitter.com/cHHillee/status/1601371640671399936))
	- In the pre-tensor-core days, your network (usually) spent all of its time doing matmuls or convs. In other words, you're compute bound (https://t.co/EGAOqVNIt5).
	  
	  And when you're compute bound, you're calling CuBLAS. Which performs the same with eager or graphs.
	  
	  (3/10) ([View Tweet](https://twitter.com/cHHillee/status/1601371642260705280))
	- So, if 90% of your network's time is spent in matmuls, then it's no big deal if you give up 10% in performance in exchange for a better UX.
	  
	  But then... Nvidia added tensor cores. And ever since, they've been relentlessly doubling or tripling FLOPS every generation.
	  
	  (4/10) 
	  
	  ![](https://pbs.twimg.com/media/FjkqgJ8VUAAN4oA.jpg) ([View Tweet](https://twitter.com/cHHillee/status/1601371646756933632))
	- So, if you go for eager-mode and leave 10% performance on the table, who cares! But if you're leaving 100%... that's a bit more problematic. And the way that performance is trending, the performance gaps from using only eager-mode are just going to get worse.
	  
	  (5/10) ([View Tweet](https://twitter.com/cHHillee/status/1601371648669515777))
	- Let's take a look at a simple MLP, and turn on/off tf32 to emulate older hardware. I've highlighted the matmuls grey.
	  
	  With tf32 off, there's not that much to optimize! We're spending 85% of our time doing matmuls, and the last 15% of our time in layernorm/relu.
	  
	  (6/10) 
	  
	  ![](https://pbs.twimg.com/media/Fjk0LDaUYAACUc0.jpg) ([View Tweet](https://twitter.com/cHHillee/status/1601371651538460673))
	- But with TF32 on, it looks like this. Note that the black bars are *exactly* the same length. But now that our matmuls are wayyy faster, we're now spending 60%!! of our time in layer norms/relu (up from 15% before). And so, there's way more room to speed things up.
	  
	  (7/10) 
	  
	  ![](https://pbs.twimg.com/media/Fjk0rAjVsAAmmU2.png) ([View Tweet](https://twitter.com/cHHillee/status/1601371655305318403))
	- @GuggerSylvain suggested that you need to enable tf32 if you want any real performance improvements. And that's true... because not using tf32 is basically bringing your hardware performance back to 2017!
	  
	  https://t.co/RgehO2wFRh
	  
	  (8/10) ([View Tweet](https://twitter.com/cHHillee/status/1601371657192382464))
	- TL;DR: PyTorch came out in a time where graph-mode compilation couldn't provide significant performance wins due to models being bottlenecked by matmuls.
	  
	  5 years of Nvidia matmul perf improvements later, graph-mode compilation can bring significant wins.
	  
	  (9/10) ([View Tweet](https://twitter.com/cHHillee/status/1601371658941779968))
	- It's unfortunate that graph-mode compilation necessitates additional complexity, but luckily, eager-mode isn't going anywhere! It'll still be ... reasonably fast. 
	  
	  But if PyTorch wanted to keep up with where the hardware's going, PyTorch 2.0 needed to happen :)
	  
	  (10/10) ([View Tweet](https://twitter.com/cHHillee/status/1601371660380086272))