title:: At the Product Retreat,... (highlights)
author:: [[@amix3k on Twitter]]
full-title:: "At the Product Retreat,..."
category:: #tweets
url:: https://twitter.com/amix3k/status/1634126513615380482

- Highlights first synced by [[Readwise]] [[Mar 12th, 2023]]
	- At the product retreat, we used GPT-3 to understand why customers cancel their paid Todoist accounts.
	  
	  Here’s a small write-up of how this works and how you could utilize this to get valuable insights into improving your products. 🤖 ([View Tweet](https://twitter.com/amix3k/status/1634126513615380482))
		- **Note**: Thread
	- It’s critical to note that you won’t be able to feed data to GPT-3 because there is a token limit (e.g., 4096 tokens for Davinci). You also won’t be able to fine-tune the custom model because fine-tuning only works for prompt+completion optimization. ([View Tweet](https://twitter.com/amix3k/status/1634126516941385733))
	- What you can use is something like LlamaIndex, which provides indices over unstructured and structured data for use with LLM’s like GPT-3. This makes it possible to query large amount of data! ([View Tweet](https://twitter.com/amix3k/status/1634126519609049091))
	- With LlamaIndex, we indexed all the data on why people canceled Todoist Pro and Todoist business. These were thousands of inputs we’ve gathered over the years. 
	  
	  This is done by a small Python script you can get from here https://t.co/uXsoqEt2Mr 
	  
	  ![](https://pbs.twimg.com/media/Fq2Vam6WYAQCToT.jpg) ([View Tweet](https://twitter.com/amix3k/status/1634126530413490181))
	- Voila, this gives you a way to query customer feedback. We’ve tested this a bit, and it confirms a lot of the knowledge we already know.
	  
	  We can ask questions like:
	  
	  — Why are customers switching to competitor X
	  — What are the top 10 things we should add to Todoist Pro
	  — etc. 
	  
	  ![](https://pbs.twimg.com/media/Fq2VbHJXgAAfXJ6.jpg) ([View Tweet](https://twitter.com/amix3k/status/1634126538206478336))