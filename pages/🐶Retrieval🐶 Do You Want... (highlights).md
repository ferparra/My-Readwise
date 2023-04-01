title:: 🐶Retrieval🐶 Do You Want... (highlights)
author:: [[@hwchase17 on Twitter]]
full-title:: "🐶Retrieval🐶 Do You Want..."
category:: #tweets
url:: https://twitter.com/hwchase17/status/1639291011942989824

- Highlights first synced by [[Readwise]] [[Mar 25th, 2023]]
	- 🐶Retrieval🐶
	  
	  Do you want to use external retrievers (like ChatGPT Retrieval Plugin) in @LangChainAI?
	  
	  Do you want to experiment with alternative retrieval methods (like hybrid search)?
	  
	  We just updated LangChain abstractions to allow for this: https://t.co/DU3NLUvxX7
	  
	  🧵 ([View Tweet](https://twitter.com/hwchase17/status/1639291011942989824))
		- **Note**: Thread
	- Previously, all chains did retrieval through the VectorDB LangChain object
	  
	  We realized this made it hard to:
	  
	  1. Use chains with retrievers constructed outside of LangChain
	  
	  2. Experiment with retrieval methods that we're semantic search ([View Tweet](https://twitter.com/hwchase17/status/1639291013431984134))
	- As such, we refactored all `VectorDB` chains to now be `Retrieval` chains
	  
	  This is done in a backwards compatible way, but we would suggest updating ASAP
	  
	  We hope this encourages more experimentation with alternative retrieval methods! ([View Tweet](https://twitter.com/hwchase17/status/1639291014707032069))