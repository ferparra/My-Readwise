title:: How to Best Build an Age... (highlights)
author:: [[@hwchase17 on Twitter]]
full-title:: "How to Best Build an Age..."
category:: #tweets
url:: https://twitter.com/hwchase17/status/1646255350386130945

- Highlights first synced by [[Readwise]] [[Apr 13th, 2023]]
	- How to best build an agent that has access to ALL the ChatGPT Plugins?
	  
	  IMO, by combining two techniques we recently introduced in @LangChainAI 
	  
	  🔧 Tool Retrieval
	  🗣️ Natural Language APIs
	  
	  Explanation and example notebook in 🧵 
	  
	  ![](https://pbs.twimg.com/media/FtisfG_aIAEMWfB.jpg) 
	  
	  ![](https://pbs.twimg.com/media/Ftisf8BaMAE1GCT.jpg) ([View Tweet](https://twitter.com/hwchase17/status/1646255350386130945))
		- **Note**: Thread
	- What are some challenges/issues that arise if you try to build an agent that has access to all the ChatGPT plugins?
	  
	  First, there will (hopefully) be MANY plugins - too many to fit in context
	  
	  Second, the LLM has to know how to properly use the underlying OpenAPI spec ([View Tweet](https://twitter.com/hwchase17/status/1646255353028571136))
	- 🔧 Tool Retrieval
	  
	  In order to combat the issue of too many plugins, we can do a retrieval step to select the relevant plugins for a given query
	  
	  This is an idea we recently shared, made easy by the recent CustomAgent refactor https://t.co/lQFpMUGzrP ([View Tweet](https://twitter.com/hwchase17/status/1646255356090400769))
	- 🗣️ Natural Language APIs
	  
	  Once the plugins are retrieved, we need to get to make sure the LLM is actually able to use the underlying API
	  
	  Anecdotally, we found the best way to achieve this was to wrap each API in a Natural Language API 
	  
	  https://t.co/msbPad0lqP ([View Tweet](https://twitter.com/hwchase17/status/1646255358250455040))
	- Why is this the case?
	  
	  We saw that most models struggled to learn/remember how to use more than one API endpoint reliably when it was put directly in the prompt
	  
	  Now the agent can just "route" requests to the right API, and the translation to actual API params happens lower down ([View Tweet](https://twitter.com/hwchase17/status/1646255359873675264))
	- Putting this all together:
	  
	  An agent that fetches relevant plugins, then creates natural language APIs for the endpoints
	  
	  See example notebook below!
	  
	  https://t.co/9M3qD8LGmQ ([View Tweet](https://twitter.com/hwchase17/status/1646255361224249344))