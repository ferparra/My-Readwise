title:: Welcome to LlamaIndex 🦙 (GPT Index)! (highlights)
author:: [[gpt-index.readthedocs.io]]
full-title:: "Welcome to LlamaIndex 🦙 (GPT Index)!"
category:: #articles
url:: https://gpt-index.readthedocs.io/en/latest/
tags:: #[[LLMs]]

- Highlights first synced by [[Readwise]] [[Apr 7th, 2023]]
	- That’s where the **LlamaIndex** comes in. LlamaIndex is a simple, flexible interface between your external data and LLMs. It provides the following tools in an easy-to-use fashion: ([View Highlight](https://read.readwise.io/read/01gxcg16sxqgdyck51jmxatjqr))
	- Provides **indices** over your unstructured and structured data for use with LLM’s. These indices help to abstract away common boilerplate and pain points for in-context learning: ([View Highlight](https://read.readwise.io/read/01gxcg19xtw4y57kqv6eysw4s7))
	- Storing context in an easy-to-access format for prompt insertion. ([View Highlight](https://read.readwise.io/read/01gxcg1av00dqhc0v3ad6b82yw))
	- Dealing with prompt limitations (e.g. 4096 tokens for Davinci) when context is too big. ([View Highlight](https://read.readwise.io/read/01gxcg1bkm9sgjg03f2wgekxpv))
	- Dealing with text splitting. ([View Highlight](https://read.readwise.io/read/01gxcg1dbw1j22vze7qyjgrb0t))
	- Context[](https://gpt-index.readthedocs.io/en/latest#context)
	  
	  •   LLMs are a phenomenonal piece of technology for knowledge generation and reasoning. They are pre-trained on large amounts of publicly available data.
	    
	  •   How do we best augment LLMs with our own private data?
	    
	  •   One paradigm that has emerged is *in-context* learning (the other is finetuning), where we insert context into the input prompt. That way, we take advantage of the LLM’s reasoning capabilities to generate a response ([View Highlight](https://read.readwise.io/read/01gxa3296pgge50eyv44je96ch))
	- Proposed Solution[](https://gpt-index.readthedocs.io/en/latest#proposed-solution)
	  
	  That’s where the **LlamaIndex** comes in. LlamaIndex is a simple, flexible interface between your external data and LLMs. It provides the following tools in an easy-to-use fashion:
	  
	  •   Offers [data connectors](http://llamahub.ai) to your existing data sources and data formats (API’s, PDF’s, docs, SQL, etc.)
	    
	  •   Provides **indices** over your unstructured and structured data for use with LLM’s. These indices help to abstract away common boilerplate and pain points for in-context learning:
	    
	    > •   Storing context in an easy-to-access format for prompt insertion.
	    >     
	    > •   Dealing with prompt limitations (e.g. 4096 tokens for Davinci) when context is too big.
	    >     
	    > •   Dealing with text splitting.
	    >     
	    
	  •   Provides users an interface to **query** the index (feed in an input prompt) and obtain a knowledge-augmented output.
	    
	  •   Offers you a comprehensive toolset trading off cost and performance. ([View Highlight](https://read.readwise.io/read/01gxa32e2hh9s59w051xz4831f))