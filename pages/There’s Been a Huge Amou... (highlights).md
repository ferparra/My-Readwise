title:: There’s Been a Huge Amou... (highlights)
author:: [[@jerryjliu0 on Twitter]]
full-title:: "There’s Been a Huge Amou..."
category:: #tweets
url:: https://twitter.com/jerryjliu0/status/1643763618629193729

- Highlights first synced by [[Readwise]] [[Apr 7th, 2023]]
	- There’s been a huge amount of interest in “hybrid” search in data retrieval + LLM’s.
	  
	  @gpt_index’s graph abstractions are one ex of hybrid search over doc collections. 🛠️
	  
	  What if you blended the simplicity/flexibility of keyword lookup with intelligence of semantic search? 💡🧵 
	  
	  ![](https://pbs.twimg.com/media/Fs_STAEaMAATcsw.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1643763618629193729))
		- **Note**: Thread
	- A simple example: you have a collection of documents, where each document corresponds to a city. 
	  
	  Each city has a simple description “Article about {city}”.
	  
	  You want to ask questions that compare/contrast different cities 🤔 ([View Tweet](https://twitter.com/jerryjliu0/status/1643763621279965184))
	- First, it makes sense to define a vector index for each document. Text chunks are organized per doc.
	  
	  Second, using our graph abstractions, you can define a “top-level” index using a simple keyword lookup! 
	  
	  ![](https://pbs.twimg.com/media/Fs_STlJaMAAiq6o.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1643763625486872576))
	- E.g. given the q “Compare and contrast the demographics in Seattle, Houston, and Toronto.”, we can match on “Houston”, “Seattle”, and “Toronto”, and route the query to the subindexes. 
	  
	  The responses will then be retrieved from subindexes. 
	  
	  ![](https://pbs.twimg.com/media/Fs_ST45aUAEffDN.jpg) 
	  
	  ![](https://pbs.twimg.com/media/Fs_ST44aAAIBQXw.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1643763632185155584))
	- A thought ❓: why do you need a keyword lookup to fetch documents? What if you just did semantic search? 
	  
	  You totally could! 
	  
	  Tradeoffs are: a bit more complex. You’d need to tune a top-k or similarity score to make sure you get relevant docs. ([View Tweet](https://twitter.com/jerryjliu0/status/1643763634202644480))
	- Check out the notebook here! https://t.co/VUIDXTMe10 ([View Tweet](https://twitter.com/jerryjliu0/status/1643763636463341568))