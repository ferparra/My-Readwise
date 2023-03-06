title:: ✨Agents + Vectorstores✨:... (highlights)
author:: [[@hwchase17 on Twitter]]
full-title:: "✨Agents + Vectorstores✨:..."
category:: #tweets
url:: https://twitter.com/hwchase17/status/1629929531678265344

- Highlights first synced by [[Readwise]] [[Feb 28th, 2023]]
	- ✨Agents + Vectorstores✨: a powerful combo
	  
	  Can be used to:
	  🍴 route questions between MULTIPLE indexes
	  ⛓️ do chain-of-thought reasoning with proprietary indexes
	  🔧 combine proprietary data with tool usage
	  
	  Here's how to use them together in @LangChainAI  👇 ([View Tweet](https://twitter.com/hwchase17/status/1629929531678265344))
		- **Note**: Thread
	- Step one is creating a query interface over your indexes
	  
	  LangChain provides easy tools for ingesting, splitting, indexing, and then querying data with a VectorDBQAChain
	  
	  Python Guide: https://t.co/CuSjPbVmLR
	  
	  JavaScript Guide: https://t.co/wVtgeEKR0L ([View Tweet](https://twitter.com/hwchase17/status/1629929532873666560))
	- Using this VectorDBQAChain *as a tool itself* in an agentic framework can unlock a lot more powerful cases
	  
	  Here are guides for using a chain as a tool:
	  
	  Python Guide: https://t.co/qYGxfdBa58
	  
	  JavaScript Guide: https://t.co/c1ydaJhNeC ([View Tweet](https://twitter.com/hwchase17/status/1629929534245187584))
	- 🍴 Route questions between MULTIPLE indexes
	  
	  If you've got multiple different indexes, you can use them each as tools
	  
	  The agent can then use its reasoning framework (ReAct, etc) to choose between indexes to query
	  
	  Detailed Docs: https://t.co/R31r66pBmT 
	  
	  ![](https://pbs.twimg.com/media/Fp6qn_GaIAAezX2.jpg) 
	  
	  ![](https://pbs.twimg.com/media/Fp6qn_EaQAA2LIu.jpg) 
	  
	  ![](https://pbs.twimg.com/media/Fp6qn_FaIAAuRmf.jpg) ([View Tweet](https://twitter.com/hwchase17/status/1629929535520272384))
	- ⛓️ Chain-of-thought reasoning with proprietary indexes
	  
	  One of the powerful things about agents is their ability to reason step-by-step (ReAct, Self-ask-with-search)
	  
	  You can easily use VectorDBQAChain to answer these intermediate steps
	  
	  Docs: https://t.co/ERiOQ7TJ8t 
	  
	  ![](https://pbs.twimg.com/media/Fp6rOA9acAA-DNU.jpg) ([View Tweet](https://twitter.com/hwchase17/status/1629929538707943425))
	- 🔧 combine proprietary data with tool usage
	  
	  Now that VectorDBQAChain is just a another tool, you can easily use it with another tool
	  
	  Eg: combine it with a slack tool and ask the agent to lookup an answer and then send it to someone over slack ([View Tweet](https://twitter.com/hwchase17/status/1629929541702680578))
	- What other use cases do you think are unlocked by combining agents with vectorstores?
	  
	  Let us know and we'll put together some examples for them! ([View Tweet](https://twitter.com/hwchase17/status/1629929542914822149))