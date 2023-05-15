title:: Memory in @LangChainAI is a big deal (highlights)
author:: [[peter! 🥷]]
full-title:: "Memory in @LangChainAI is a big deal"
category:: #articles
url:: https://twitter.com/pwang_szn/status/1656600055770681345
document_note:: Memory plays a significant role in @LangChainAI. The different types of memory include ConversationBufferMemory, ConversationBufferWindowMemory, ConversationSummaryMemory, and VectorStore-Backed Memory. Each memory type has its benefits, such as storing messages, keeping memory history small, creating conversation summaries, and storing memories in a VectorDB. Memory can be added to a chain, agent, or even multi-input chain to improve AI's ability to remember relevant information. Further demo projects with memory will be made in the coming weeks.

- Highlights first synced by [[Readwise]] [[May 15th, 2023]]
	- ![](https://pbs.twimg.com/media/Fv1s-F6acAU2kOn.jpg) ([View Highlight](https://read.readwise.io/read/01h07rfckncn0mbj5940pwexw1))
		- **Tags**: #[[visual mapping]] #[[langchain]]
	- ConversationSummaryMemory
	  
	  • Creates a summary of the conversation over time.
	  
	  Pro: Useful for condensing information from the conversation over time. ([View Highlight](https://read.readwise.io/read/01h07retvfk67t7ak72bjkrz0k))
	- VectorStore-Backed Memory
	  
	  • Stores memories in a VectorDB  
	  • Queries the top-K most relevant docs
	  
	  Pro:
	- How to Add Memory to a Chain
	  
	  1) Setup Prompt and Memory  
	  2) Initialize LLMChain  
	  3) Call the LLMChain ([View Highlight](https://read.readwise.io/read/01h07rf47bk7cv964fvjg7nm92))