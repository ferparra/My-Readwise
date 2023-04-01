title:: How Do You Measure the Q... (highlights)
author:: [[@jerryjliu0 on Twitter]]
full-title:: "How Do You Measure the Q..."
category:: #tweets
url:: https://twitter.com/jerryjliu0/status/1641234014991446016

- Highlights first synced by [[Readwise]] [[Mar 31st, 2023]]
	- How do you measure the query performance/hallucination on @gpt_index *without* ground-truth labels? 🤔
	  
	  Compare the synthesized text response with the retrieved sources! 
	  
	  Our new *evaluation module* allows you to do exactly that. Check out details below 🧵 
	  
	  ![](https://pbs.twimg.com/media/FsbVoyqaUAAqoTO.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1641234014991446016))
		- **Note**: Thread
	- When you query a @gpt_index data structure, you get back a synthesized response + retrieved sources.
	  
	  To evaluate: make another LLM call to see if response is supported by the sources.
	  
	  If at least one source matches, then you’re good ✅. If not, there may be hallucination! ⚠️ ([View Tweet](https://twitter.com/jerryjliu0/status/1641234017348653056))
	- But wait: what if you have a *lot* of sources to go through? So much that it’s bigger than the context window? 
	  
	  No problem: simply store the sources in our list index data structure 💪 ([View Tweet](https://twitter.com/jerryjliu0/status/1641234019298967552))
	- Here’s an example. We query our tree index 🎄, and run our evaluation module: check if the synthesized response matches the sources.
	  
	  Although the response is objectively correct, the source contains unrelated context (from 2015) - indicating hallucination! 
	  
	  ![](https://pbs.twimg.com/media/FsbVpWbacAARb4u.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1641234023401033729))
	- Here’s another example: We query our vector index, and also run our evaluation module.
	  
	  We see that for both questions, the response matches the retrieved context, which is a good thing ⭐️ 
	  
	  ![](https://pbs.twimg.com/media/FsbVpmwaQAACcIW.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FsbVpmxaMAIzw0f.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1641234028631302144))
	- Check out our full notebook here: https://t.co/cYPuNhoVC1.
	  
	  A HUGE shoutout to @ravithejads for building this awesome feature 🔥🙌 ([View Tweet](https://twitter.com/jerryjliu0/status/1641234030619410433))