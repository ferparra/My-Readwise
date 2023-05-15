title:: An Implication of Design... (highlights)
author:: [[@jerryjliu0 on Twitter]]
full-title:: "An Implication of Design..."
category:: #tweets
url:: https://twitter.com/jerryjliu0/status/1652704323678375936

- Highlights first synced by [[Readwise]] [[May 1st, 2023]]
	- An implication of designing any LLM app over your data is you’re adding “state” (data) to a “stateless” module (LLM).
	  
	  Stateful apps are hard, and require good storage abstractions.
	  
	  We’ve thought hard about this with @gpt_index 🧵 
	  
	  ![](https://pbs.twimg.com/media/Fu-V0wsacAMo6Qa.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1652704323678375936))
		- **Note**: Thread
	- Hacking an initial retrieval-augmented LLM app is super easy: take some documents, chunk it up, put it in a vector db.
	  
	  But thinking about prod data reqs makes this more challenging.
	  
	  It’s one thing to build a demo over 5 docs. What about over GB’s of data over different sources? ([View Tweet](https://twitter.com/jerryjliu0/status/1652704325272207362))
	- Some questions:
	  
	  How do we store source Documents? Once we split it, how do we store text chunks? 
	  
	  How do we store metadata? Including indices on your data?
	  
	  How do we store vectors with vector db’s? ([View Tweet](https://twitter.com/jerryjliu0/status/1652704326551482368))
	- The new release of @gpt_index (0.6.0) takes a stab at addressing this:
	- There is now a vector ecosystem of vector db providers. Many vector db’s (e.g. @pinecone, @trychroma, @weaviate_io), allow storage of both vectors and docs.
	  
	  For now they’re sep from our docstore; we have a TODO to explore similarities. ([View Tweet](https://twitter.com/jerryjliu0/status/1652704329118384129))
	- A key concept is to decouple the raw data from the indexes that we define at the top-level.
	  
	  An Index in @gpt_index is just a lightweight view over your data, each solving a diff retrieval use case.
	  
	  You can/should define multiple indices over your data. ([View Tweet](https://twitter.com/jerryjliu0/status/1652704330431205376))
	- Interested in contributing? We’d LOVE to have your help in building way more document store abstractions: S3, GCS, HDFS, and more.
	  
	  + more vector integrations as well. 
	  
	  https://t.co/OMXchrDSmL ([View Tweet](https://twitter.com/jerryjliu0/status/1652704331773394946))