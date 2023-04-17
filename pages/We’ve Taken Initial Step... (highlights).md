title:: We’ve Taken Initial Step... (highlights)
author:: [[@jerryjliu0 on Twitter]]
full-title:: "We’ve Taken Initial Step..."
category:: #tweets
url:: https://twitter.com/jerryjliu0/status/1642908812771471360

- Highlights first synced by [[Readwise]] [[Apr 7th, 2023]]
	- We’ve taken initial steps to improve LLM + retrieval capabilities in a BIG direction:
	  
	  Temporal reasoning over your data! ⏳
	  
	  @gpt_index can now infer whether your query involves searching over previous/future Nodes, and fetch more accordingly 👇 
	  
	  ![](https://pbs.twimg.com/media/FszI26laYAEgOHK.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1642908812771471360))
		- **Note**: Thread
	- One downside of top-k retrieval is that the retrieved context may match the query in embedding similarity, but not answer it.
	  
	  E.g. “What did the author do after his time at YC”, will retrieve context during his time at YC. 
	  
	  But the answer is found in “future” contexts. ([View Tweet](https://twitter.com/jerryjliu0/status/1642908815199981568))
	- We’ve introduced a NodePostprocessor class to help with this! e.g.
	  
	  1.First retrieve context (Nodes) from your index (e.g. top-k lookup) 
	  2.Decide whether we need to look more in the future 🔮 or past 📜
	  3.Fetch more Nodes accordingly 
	  
	  ![](https://pbs.twimg.com/media/FszI3S-acAMqCjU.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1642908819872436225))
	- Take a look at this example below.
	  
	  With the node postprocessor we are able to answer the above question in detail (left 🖼️).
	  
	  Without it, we don’t get back a satisfactory answer (even if we increase the top-k): (middle/right 🖼️) 
	  
	  ![](https://pbs.twimg.com/media/FszI3oAaIAEgOa3.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FszI3m2aYAAXpRr.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FszI3m6aIAAOtIf.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1642908827199873026))
	- Check out the notebook here: https://t.co/7coEkSCiq2
	  
	  NOTE: this is a beta feature, the API interface might change in the future! ([View Tweet](https://twitter.com/jerryjliu0/status/1642908830093934592))