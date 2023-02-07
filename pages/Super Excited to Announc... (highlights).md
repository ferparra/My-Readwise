title:: Super Excited to Announc... (highlights)
author:: [[@jerryjliu0 on Twitter]]
full-title:: "Super Excited to Announc..."
category:: #tweets
url:: https://twitter.com/jerryjliu0/status/1608632335695745024

- Highlights first synced by [[Readwise]] [[Feb 4th, 2023]]
	- Super excited to announce that we’ve worked hard on adding a 🎉 comprehensive guide 🎉 to using @gpt_index! https://t.co/3yyjNl7Guy
	  
	  Have gotten questions on what use cases GPT Index can support - it can support a lot! This guide is a big step towards answering that 👇 ([View Tweet](https://twitter.com/jerryjliu0/status/1608632335695745024))
		- **Note**: Thread
	- At its core, GPT Index is about:
	  
	  1. loading in external data (@NotionHQ, @Slack, .txt, etc.)
	  2. Building indices over that data
	  3. Inputting a prompt -> getting an output! 
	  
	  Details are in our usage pattern guide: https://t.co/HFmMqigr9v ([View Tweet](https://twitter.com/jerryjliu0/status/1608632337063084033))
	- This simple paradigm unlocks a lot of use cases: https://t.co/yS9LcKDY2D
	  
	  
	  (1) Our vector store indices allow you to easily get relevant external data from your db to plugin to an LLM. Can be used for question-answering, text generation, and more! 
	  
	  ![](https://pbs.twimg.com/media/FlMBgfSacAMQIBk.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1608632338292047873))
	- (2) You also easily perform *summarization queries* over entire collections of documents.
	  
	  We offer different response modes (create and refine, tree summarization), allowing you to synthesize summaries in different ways! 
	  
	  ![](https://pbs.twimg.com/media/FlMBjxYaAAUwUw8.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1608632339671941124))
	- (3) You can synthesize an answer across heterogeneous data collections.
	  
	  Say you want to use both @NotionHQ and @SlackHQ data to answer your question. Using index composability, you can define subindices for @NotionHQ/@SlackHQ, and define a top-level list index to combine them. 
	  
	  ![](https://pbs.twimg.com/media/FlMBnv-acAAJ8de.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1608632341064486918))
	- (4) You can define top-level routers (for instance, using the Tree Index or Keyword Table Index), to route queries to the right index.
	  
	  Using the previous example with @NotionHQ/@SlackHQ as subindices, you can define a top-level router on top of it! 
	  
	  ![](https://pbs.twimg.com/media/FlMBqLaaYAAWSrr.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1608632342373072896))
	- You may ask: What happened to the OG Tree Index 🌲? Is this still being used? 
	  
	  We’ve found that the tree index is effective as a routing tool. But we also offer much more functionality that is captured by our wider set of indices now. ([View Tweet](https://twitter.com/jerryjliu0/status/1608632343761412096))
	- GPT Index’s general ability to *compose* indices (https://t.co/9MUV9hDP9Z), captured in the use cases above, can be seen as a generalization of the tree index. 
	  
	  You now have control in indexing the overall “graph” structure of your data that best suits your LLM needs 🛠️ ([View Tweet](https://twitter.com/jerryjliu0/status/1608632344914857984))
	- Are there additional use cases that you want from GPT Index to best connect GPT with your data? Do you want help using GPT Index features? Let us know! 
	  
	  Stoked about the potential LLM applications that make use of these abstractions.
	  
	  P.S. There will be a Discord soon! ([View Tweet](https://twitter.com/jerryjliu0/status/1608632346143756288))
	- @dbenyamin @gpt_index Of course, langchain is a general LLM toolkit and offers some of this stuff already (like data connections, response synthesis, etc.). But that is largely GPT Index's focus. 
	  
	  Langchain offers broader stuff like interactive agent reasoning, and evaluation framework, and more. ([View Tweet](https://twitter.com/jerryjliu0/status/1608645839463010304))
	- @dbenyamin @gpt_index GPT Index uses langchain under the hood so the cost of using both shouldn't be too high. There's prob broader integration opportunities as well. cc @hwchase17 to chime in though! ([View Tweet](https://twitter.com/jerryjliu0/status/1608646120892411907))