title:: 🤖🔧Agent ToolKits🤖🔧 Http... (highlights)
author:: [[@LangChainAI on Twitter]]
full-title:: "🤖🔧Agent ToolKits🤖🔧 Http..."
category:: #tweets
url:: https://twitter.com/LangChainAI/status/1630965778345504768

- Highlights first synced by [[Readwise]] [[Mar 6th, 2023]]
	- 🤖🔧Agent ToolKits🤖🔧
	  
	  https://t.co/kOe2SaUYao
	  
	  Collections of tools aimed at allowing an agent to best interact with a particular resource. Eg:
	  
	  🧱 SQL DBs
	  🔄 APIs
	  🐍 Python REPL
	  Others!
	  
	  Allows them to use complex resources and recover from mistakes
	  
	  Some 🤯 examples 👇 ([View Tweet](https://twitter.com/LangChainAI/status/1630965778345504768))
		- **Note**: Thread
	- 🧱 SQL DBs
	  
	  This agent builds off of SQLDatabaseChain, but is designed to work on larger databases and be fault tolerant
	  
	  Tools include: get table names, get metadata for a table, create query, fix query
	  
	  Python: https://t.co/0yJcRJvOsA
	  JS: https://t.co/hVgG0GFmx7 ([View Tweet](https://twitter.com/LangChainAI/status/1630965779700256770))
	- In the example below, it:
	- 🔄 APIs
	  
	  Give the agent an OpenAPI spec and have it figure out how to use it
	  
	  Tools: A json agent to explore the spec and come up with a request, a requests tool to execute requests
	  
	  Python: https://t.co/49VBgBaSET
	  JS: https://t.co/lB7Md10JGp ([View Tweet](https://twitter.com/LangChainAI/status/1630965783605166081))
	- In the below example, we are using the OpenAPI spec for the OpenAI API
	  
	  The agent first sifts through the JSON representation of the spec, find the required base URL, path, required parameters for  a POST request to the /completions endpoint
	  
	  It then makes the request 
	  
	  ![](https://pbs.twimg.com/media/FqJYD_CaQAAHTax.jpg) ([View Tweet](https://twitter.com/LangChainAI/status/1630965785324834817))
	- 🐍 Python REPL
	  
	  This toolkit consists of a Python REPL, and by interacting with it in an iterative way it can recover from errors and do more complex things
	  
	  Some examples popped up in the last in the community of it doing exactly this: ([View Tweet](https://twitter.com/LangChainAI/status/1630965788361515008))
	- In @lemonodor's example it tries to use a fibonacci function that doesn't exists, so it errors
	  
	  It then writes the function and uses it
	  
	  https://t.co/kV59UoYWqy ([View Tweet](https://twitter.com/LangChainAI/status/1630965790051811328))
	- In @sameeurehman's example it writes a neural network in Pytorch and then uses it to do inference correctly
	  
	  https://t.co/uOemKjTTrB ([View Tweet](https://twitter.com/LangChainAI/status/1630965791746314241))
	- We've added this as toolkit as well
	  
	  Python: https://t.co/ky6CPrzEKw
	  
	  Note that the examples may be different than the tweets, as we tweaked the agent's prompts to give it better instructions ([View Tweet](https://twitter.com/LangChainAI/status/1630965793461764096))
	- Other toolkits include:
	- We provide these toolkits not because we think they're perfect for all use cases, but because we hope
	  
	  1. they are enough to get started
	  2. they inspire people to create other/better ones
	  
	  What toolkits would you like to see next? Which ones are you going to build? ([View Tweet](https://twitter.com/LangChainAI/status/1630965796821417984))