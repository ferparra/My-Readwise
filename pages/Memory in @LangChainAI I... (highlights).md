title:: Memory in @LangChainAI I... (highlights)
author:: [[@pwang_szn on Twitter]]
full-title:: "Memory in @LangChainAI I..."
category:: #tweets
url:: https://twitter.com/pwang_szn/status/1656600055770681345

- Highlights first synced by [[Readwise]] [[May 15th, 2023]]
	- Memory in @LangChainAI is a big deal.
	  
	  It was a lot to go through, but I broke it into bite-size chunks.
	  
	  • 4 Memory Types Explained
	  • How to use Memory in a Chain
	  • How to add Memory to an Agent
	  
	  Save this ↓ 
	  
	  ![](https://pbs.twimg.com/media/Fv1s-F6acAU2kOn.jpg) ([View Tweet](https://twitter.com/pwang_szn/status/1656600055770681345))
		- **Note**: Thread
	- ConversationBufferMemory:
	  
	  • Memory allows for storing of messages
	  • Extracts the messages in a variable.
	  
	  Pro: Basic to understand/pickup 
	  
	  ![](https://pbs.twimg.com/media/Fv1s-a3aYAEI6Mx.jpg) ([View Tweet](https://twitter.com/pwang_szn/status/1656600063005851651))
	- ConversationBufferWindowMemory:
	  
	  • Only uses the last K messages.
	  
	  Pro: Useful to keep the memory history small 
	  
	  ![](https://pbs.twimg.com/media/Fv1s-2jaAAEhcFN.jpg) ([View Tweet](https://twitter.com/pwang_szn/status/1656600070446522370))
	- ConversationSummaryMemory
	  
	  • Creates a summary of the conversation over time.
	  
	  Pro: Useful for condensing information from the conversation over time. 
	  
	  ![](https://pbs.twimg.com/media/Fv1s_R6aYAEHyt0.jpg) ([View Tweet](https://twitter.com/pwang_szn/status/1656600077623001090))
	- VectorStore-Backed Memory
	  
	  • Stores memories in a VectorDB
	  • Queries the top-K most relevant docs
	  
	  Pro:
	- How to Add Memory to a Chain
	  
	  1) Setup Prompt and Memory
	  2) Initialize LLMChain
	  3) Call the LLMChain 
	  
	  ![](https://pbs.twimg.com/media/Fv1tAJFaYAAhxXu.jpg) ([View Tweet](https://twitter.com/pwang_szn/status/1656600092655374337))
	- How to Add Memory to an Agent
	  
	  1) Create an LLMChain with memory.
	  2) Use the LLMChain to create a custom Agent. 
	  
	  ![](https://pbs.twimg.com/media/Fv1tAkoaYAAgyyE.jpg) ([View Tweet](https://twitter.com/pwang_szn/status/1656600101094313985))
	- How to Add Memory to Multi-Input Chain: 
	  
	  ![](https://pbs.twimg.com/media/Fv1tBF-aMAI7Xrr.jpg) ([View Tweet](https://twitter.com/pwang_szn/status/1656600109952688131))
	- Last but not least:
	  
	  It's also possible to combine memory classes in the same chain: 
	  
	  ![](https://pbs.twimg.com/media/Fv1tBngacAAkHlq.jpg) ([View Tweet](https://twitter.com/pwang_szn/status/1656600118387417088))
	- That's it!
	  
	  Will be making a lot more demo projects with memory in the upcoming weeks! 🫡 ([View Tweet](https://twitter.com/pwang_szn/status/1656600121566691328))