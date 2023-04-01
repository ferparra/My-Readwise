title:: Retrieval (highlights)
author:: [[LangChain]]
full-title:: "Retrieval"
category:: #articles
url:: https://blog.langchain.dev/retrieval/
tags:: #[[ai]] #[[langchain]]

- Highlights first synced by [[Readwise]] [[Mar 28th, 2023]]
	- ![](https://blog.langchain.dev/content/images/2023/03/image-1.png) ([View Highlight](https://read.readwise.io/read/01gwjfbgv9pddekje3scwed4wb))
		- **Tags**: #[[information retrieval]] #[[gpt]]
	- **First:** there a lot of different variations in how you do this retrieval step. People want to do things beyond semantic search. To be concrete:
	  
	  •   We support two different query methods: one that just optimizes similarity, another with optimizes for [maximal marginal relevance](https://www.cs.cmu.edu/~jgc/publication/The_Use_MMR_Diversity_Based_LTMIR_1998.pdf).
	  •   Users often want to specify metadata filters to filter results before doing semantic search
	  •   Other types of indexes, [like graphs](https://langchain.readthedocs.io/en/latest/modules/indexes/chain_examples/graph_qa.html), have piqued user's interests ([View Highlight](https://read.readwise.io/read/01gwjfcgwx52naj6mxesmkjn6h))
	- **Q: What's the difference between an index and a retriever?**
	  
	  **A:** An index is a data structure that supports efficient searching, and a retriever is the component that uses the index to find and return relevant documents in response to a user's query. The index is a key component that the retriever relies on to perform its function. ([View Highlight](https://read.readwise.io/read/01gwjfdns05staj2fdcxsq779b))
	- **Q: What are real world examples this enables?**
	  
	  **A:** The main one is better question-answering over your documents. However, if start to ingest and then retrieve previous messages, this can then be thought of as better long term memory for AI. ([View Highlight](https://read.readwise.io/read/01gwjfe62bdd9n2xgr09sy7q4j))