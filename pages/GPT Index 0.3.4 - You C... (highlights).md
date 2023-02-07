title:: GPT Index 0.3.4 - You C... (highlights)
author:: [[@gpt_index on Twitter]]
full-title:: "GPT Index 0.3.4 - You C..."
category:: #tweets
url:: https://twitter.com/gpt_index/status/1621558579403841537

- Highlights first synced by [[Readwise]] [[Feb 4th, 2023]]
	- GPT Index 0.3.4
		- **Note**: Thread
	- Recall that GPT Index allows you to define a graph structure on top of your indices, so that parent indices can "route" to child indices.
	  
	  Now you can also have more control in “fetching” the indices that make up this graph. ([View Tweet](https://twitter.com/gpt_index/status/1621558580884414466))
	- First, you can define a doc_id for each subindex (see 🖼️) 
	  
	  ![](https://pbs.twimg.com/media/FoDuj1laEAAccqs.jpg) ([View Tweet](https://twitter.com/gpt_index/status/1621558582335651840))
	- Next, we build a keyword table index over these subindices over the standard way of defining a ComposableGraph. 
	  
	  Now we can call `graph.get_index()` to fetch a subindex! (see 🖼️) You can use this subindex to run recursive or non-recursive queries. 
	  
	  ![](https://pbs.twimg.com/media/FoDum2kacAIx1Kv.png) 
	  
	  ![](https://pbs.twimg.com/media/FoDunoNaMAA-kis.png) ([View Tweet](https://twitter.com/gpt_index/status/1621558585200353282))