title:: Instead of Finding the P... (highlights)
author:: [[@ericjang11 on Twitter]]
full-title:: "Instead of Finding the P..."
category:: #tweets
url:: https://twitter.com/ericjang11/status/1639882111338573824

- Highlights first synced by [[Readwise]] [[Mar 28th, 2023]]
	- Instead of finding the perfect prompt for an LLM (let's think step by step), you can ask LLMs to critique their outputs and immediately fix their own mistakes. Here's a fun example: ([View Tweet](https://twitter.com/ericjang11/status/1639882111338573824))
		- **Note**: Thread
	- I saw @awjuliani's tweet that LLMs cannot generate a non-rhyming poem. Indeed, GPT-4 does not do it even if I ask it to think carefully 
	  https://t.co/O61PkLMmBV 
	  
	  ![](https://pbs.twimg.com/media/FsIIVJJaYAUaNoi.png) ([View Tweet](https://twitter.com/ericjang11/status/1639882382437384192))
	- @awjuliani Now you ask GPT-4 if it met the assignment, at which point it apologizes and generates a valid non-rhyming poem! full marks 
	  
	  ![](https://pbs.twimg.com/media/FsIIeHsaIAUo2vp.png) ([View Tweet](https://twitter.com/ericjang11/status/1639882699702947840))
	- @awjuliani h/t @avisingh599 for pointing me out the Reflexion paper, which gets at this idea. It's absolutely wild to me that LLMs are general enough that they can critique their own outputs in a sensible way 
	  https://t.co/UvhtPiCTaa ([View Tweet](https://twitter.com/ericjang11/status/1639882942762872832))
	- @awjuliani @avisingh599 Interestingly enough, GPT-3.5 is incapable of such self-critique, at least for this assignment. It seems to be an emergent capability only present in GPT-4 
	  
	  ![](https://pbs.twimg.com/media/FsIJYIsakAAyphp.png) ([View Tweet](https://twitter.com/ericjang11/status/1639883531336941568))
	- @awjuliani @avisingh599 The implications are substantial. Instead of clever "prefix prompt engineering", we can now consider a "postfix prompt engineering", which encourages LLMs to find corrections and inconsistencies within prior generated solutions. ([View Tweet](https://twitter.com/ericjang11/status/1639884207639134208))
	- @awjuliani @avisingh599 After any generated output, just append "did the generated output do what the user asked?" and the LLM becomes a "minimal policy improvement operator" for itself https://t.co/TYKNne61m1 ([View Tweet](https://twitter.com/ericjang11/status/1639884570240876550))
	- @awjuliani @avisingh599 Maybe it is possible to apply a critique to the critique recursively, i.e. append "is the critique logically consistent with the original request?" GPT-3.5 seems to be rather biased towards self-congratulatory optimism 
	  
	  ![](https://pbs.twimg.com/media/FsILf-kaUAAFzLD.png) ([View Tweet](https://twitter.com/ericjang11/status/1639885940754886657))
	- Wrote a quick blog post about it here.  https://t.co/Bv3B9qpt4A
	  
	  Would be curious to see what examples it can verify & correct, and what examples it can only verify, and what tasks it fails to verify ([View Tweet](https://twitter.com/ericjang11/status/1640053753645768704))
	- Also this self-critique trick seems to be able to handle @ylecun's gear puzzle! https://t.co/dLWYLS0sX9 ([View Tweet](https://twitter.com/ericjang11/status/1640078081326198784))
	- @character_ai 's c.ai@1.2 does a pretty good job without further prefix or postfix prompting 
	  
	  ![](https://pbs.twimg.com/media/FsMdEC7aYAAuCeJ.png) ([View Tweet](https://twitter.com/ericjang11/status/1640186653452156929))