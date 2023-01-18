title:: We've Been Using @Anthro... (highlights)
author:: [[@beyang on Twitter]]
full-title:: "We've Been Using @Anthro..."
category:: #tweets
url:: https://twitter.com/beyang/status/1614895568949764096

- Highlights first synced by [[Readwise]] [[Jan 17th, 2023]]
	- We've been using @AnthropicAI's new language model, Claude, to build an in-editor coding assistant called Cody that helps you understand code and reduces day-to-day sources of programmer toil.
	  
	  Here's a sneak peek 👇 
	  
	  ![](https://pbs.twimg.com/media/Fmk0dRBaMAI5wgw.jpg) ([View Tweet](https://twitter.com/beyang/status/1614895568949764096))
		- **Note**: Thread
	- Compared to other LLMs, Claude seems to go the extra mile to explain its thought process and avoid hallucinating. It also seems to have a *very* long memory.
	  
	  @goodside has great notes about how Claude stacks up for general tasks: https://t.co/JARvbVvO6f
	  https://t.co/lR1YwU5C0L ([View Tweet](https://twitter.com/beyang/status/1614895570338058242))
	- For the specific domain of code, Claude is very knowledgeable. You can ask it to generate code in a particular language, write shell commands, and explain high-level concepts. 
	  
	  ![](https://pbs.twimg.com/media/Fmk4nKXakAIvf4t.png) 
	  
	  ![](https://pbs.twimg.com/media/Fmk4o6FaMAIJvb_.jpg) 
	  
	  ![](https://pbs.twimg.com/media/Fmk4sHeaAAE-SOu.png) 
	  
	  ![](https://pbs.twimg.com/media/Fmk5z63aMAAGZOc.png) ([View Tweet](https://twitter.com/beyang/status/1614895571927707648))
	- Cody talks to Claude, but lives inside your editor. Cody can thus reference your code and answer specific questions about it that a standalone language model would not know how to answer truthfully.
	  
	  Here, Cody tells me exactly where to find Sourcegraph's outermost UI component: 
	  
	  ![](https://pbs.twimg.com/media/Fmk7ZiAagAAP9Dz.png) 
	  
	  ![](https://pbs.twimg.com/media/Fmk7bS5acAARBc5.jpg) ([View Tweet](https://twitter.com/beyang/status/1614895573366378496))
	- Once Cody has "read" a codebase, it can answer a whole bunch of questions about it. It's great for acquiring high-level context and figuring out where to dive in. 
	  
	  ![](https://pbs.twimg.com/media/Fmk7qTPaEAAoFk0.jpg) 
	  
	  ![](https://pbs.twimg.com/media/Fmk7ralagAMnfal.jpg) 
	  
	  ![](https://pbs.twimg.com/media/Fmk7s8jakAEP79V.jpg) ([View Tweet](https://twitter.com/beyang/status/1614895574758871042))
	- You can ask Cody general programming questions, too, and on reply, you can have Cody tailor answers to your specific code: 
	  
	  ![](https://pbs.twimg.com/media/Fmk74fyaMAEWqVP.jpg) 
	  
	  ![](https://pbs.twimg.com/media/Fmk75pKaYAEabrq.jpg) ([View Tweet](https://twitter.com/beyang/status/1614895576197521408))
	- Side note: much effort has gone into training Claude to avoid hallucinations, but these can still occur. Cross-checking AI-generated code with a Sourcegraph search is a good way to gut-check correctness and find additional examples. We plan to roll this skill soon into Cody. 
	  
	  ![](https://pbs.twimg.com/media/Fmk8CsVacAA0_Xd.jpg) ([View Tweet](https://twitter.com/beyang/status/1614895577556484098))
	- Since formulating the right question to ask a LLM can be a bit tricky at times, Cody provides a list of recipes for common asks. For example, you can click a button and get a high-level explanation of some hairy code: 
	  
	  ![](https://pbs.twimg.com/media/Fmk8UtYagAAaQLn.jpg) 
	  
	  ![](https://pbs.twimg.com/media/Fmk8Z1maYAA763V.png) ([View Tweet](https://twitter.com/beyang/status/1614895578856689666))
	- Here's Cody generating unit tests, taking into account codebase context like existing tests that exhibit patterns you'd like to replicate: 
	  
	  ![](https://pbs.twimg.com/media/Fmk8pH6aYAA5pqL.jpg) 
	  
	  ![](https://pbs.twimg.com/media/Fmk8qLyacAIIzuv.jpg) ([View Tweet](https://twitter.com/beyang/status/1614895580161118209))
	- We see huge potential for integrating the natural language abilities of LLMs with @sourcegraph's code search and intelligence. The early results are already super useful and we're only just getting started.
	  
	  We're rolling out Cody in a limited beta soon, DM if you'd like access! ([View Tweet](https://twitter.com/beyang/status/1614895581499125760))