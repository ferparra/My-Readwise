title:: 💡Sparse-Dense Hybrid Sea... (highlights)
author:: [[@jerryjliu0 on Twitter]]
full-title:: "💡Sparse-Dense Hybrid Sea..."
category:: #tweets
url:: https://twitter.com/jerryjliu0/status/1644489328591257600

- Highlights first synced by [[Readwise]] [[Apr 13th, 2023]]
	- 💡Sparse-Dense Hybrid Search
	  
	  One downside of semantic search is it may not generalize to new domains.
	  
	  There’s been growing interest in “hybrid” search: dense vectors + sparse “keyword” vectors.
	  
	  @gpt_index now supports this in our vector db’s! (@pinecone, @weaviate_io) 🔥👇 
	  
	  ![](https://pbs.twimg.com/media/FtJmVCvakAAl_k6.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1644489328591257600))
		- **Note**: Thread
	- @pinecone, @weaviate_io, and other db’s have support for different modes of hybrid search 🛠️
	  
	  @pinecone has an excellent blog post here: https://t.co/4TlI6CSQep
	  
	  @eddiedzhou also talked about the advantages of hybrid search during our fireside chat. ([View Tweet](https://twitter.com/jerryjliu0/status/1644489330763923456))
	- Here’s an example notebook using @pinecone’s hybrid search: 
	  
	  https://t.co/8lfAG0E9Cg
	  
	  Different vector db’s may have different interfaces for computing sparse embeddings. We aim to support them all. 
	  
	  ![](https://pbs.twimg.com/media/FtJmVa0aQAEcKE7.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1644489335071457282))
	- Here’s another example for @weaviate_io! 
	  
	  https://t.co/WT0Uowm8Gp
	  
	  Let’s compare responses with alpha=0 (pure bm25) vs. alpha=0.75 (favors vector search) 
	  
	  ![](https://pbs.twimg.com/media/FtJmVumaQAAkVg8.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FtJmVujaYAEq78r.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1644489341379678208))
	- We’re super excited: 
	  You can now unlock the full potential of search within a vector db, and also add that with some of the advanced primitives that @gpt_index offers on top: