title:: One of the Main Goals Of... (highlights)
author:: [[@jerryjliu0 on Twitter]]
full-title:: "One of the Main Goals Of..."
category:: #tweets
url:: https://twitter.com/jerryjliu0/status/1642319097928224768

- Highlights first synced by [[Readwise]] [[Apr 2nd, 2023]]
	- One of the main goals of LlamaIndex is to be really really good at retrieval + synthesis over your data. 
	  
	  Lots of users have asked what we offer beyond top-k semantic search with a vector db. Here’s a quick tour! 🧵
	  
	  https://t.co/uefnvrLzqX ([View Tweet](https://twitter.com/jerryjliu0/status/1642319097928224768))
		- **Note**: Thread
	- Basic use cases:
	  ⁃🔍Semantic Search  
	  ⁃📖Summarization
	  
	  Advanced Use Cases: 
	  ⁃📊Structured Data 
	  ⁃🧪Synthesizing Heterogeneous Data
	  ⁃🚏Routing over Heterogeneous Data
	  ⁃🍎🍊Compare/Contrast Queries
	  ⁃🪜Multi-step Queries
	  ⁃And a lot more! ([View Tweet](https://twitter.com/jerryjliu0/status/1642319099475935232))
	- 🔍 Semantic Search: The simplest thing to start with. Do top-k embedding lookup from any vector store (@pinecone, @trychroma, @weaviate, etcetc).
	  
	  The main benefit of @gpt_index here is that you can literally do semantic search over most data in 3 lines of code. 
	  
	  ![](https://pbs.twimg.com/media/FsqwhU7aUAENmfF.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1642319103380824064))
	- 📖 Summarization: Another simple thing to do. Simply define a list index over your documents, which by default will retrieve *all* nodes associated with your doc.
	  
	  Querying the list index is similarly super simple. 
	  
	  ![](https://pbs.twimg.com/media/FsqwhknaUAA4S6R.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1642319107034075136))
	- 📊 Queries over Structured Data: For those of you who liked our @huggingface streamlit demo, https://t.co/q4dBL0U0BD, you can do something similar very easily! Just follow the guide here: 
	  
	  https://t.co/q4dBL0U0BD ([View Tweet](https://twitter.com/jerryjliu0/status/1642319108699226112))
	- 🧪 Synthesizing/Routing over Heterogeneous Data: 
	  
	  By defining a graph structure, you can perform retrieval/synthesis over heterogeneous data sources (say your @NotionHQ docs or your @SlackHQ conversations. 
	  
	  Take a look at our City Analysis Demo: https://t.co/zPfElw8i4S 
	  
	  ![](https://pbs.twimg.com/media/Fsqwh3_aAAAEake.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1642319112432140288))
	- 🍎🍊 Compare/Contrast Queries:
	  
	  Once you have a graph structure over different data sources, define a query transformation module to break down a complex question into a simpler one over each data source! 
	  
	  https://t.co/0oDYAVfkuG 
	  
	  ![](https://pbs.twimg.com/media/FsqwiGBakAAliRb.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1642319116181848064))
	- Multi-Step Queries: 
	  
	  You can also ask complex questions over a single data source. Our query decomposition modules allow you to break a complex question into simpler subquestions that can be answered.
	  
	  https://t.co/GmJ6TzHMgX 
	  
	  ![](https://pbs.twimg.com/media/FsqwiUPaEAIxkfh.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FsqwiURaEAEhmDh.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1642319119650553856))
	- This is just an initial step. We’re adding a ton of new features here to optimize for different use cases (performance/storage/cost), and also new tutorials 🛠️🙌 ([View Tweet](https://twitter.com/jerryjliu0/status/1642319122099998720))