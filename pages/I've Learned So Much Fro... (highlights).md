title:: I've Learned So Much Fro... (highlights)
author:: [[@rileytomasek on Twitter]]
full-title:: "I've Learned So Much Fro..."
category:: #tweets
url:: https://twitter.com/rileytomasek/status/1603854647575384067

- Highlights first synced by [[Readwise]] [[Dec 18th, 2022]]
	- I've learned so much from @hubermanlab, but podcasts make recall and discovery challenging.
	  
	  Huberman AI uses the latest models from @openai to search every episode with Google-level accuracy and summarize the results.
	  
	  https://t.co/1nctiAIuGO https://t.co/VpjnY2NcpM ([View Tweet](https://twitter.com/rileytomasek/status/1603854647575384067))
		- **Note**: Thread
	- The search works on semantic meaning, not just keywords. This allows you to search for a term like "neurotransmitters" and get results that include "dopamine" and "serotonin."
	  
	  https://t.co/RartZqq0Cj 
	  
	  ![](https://pbs.twimg.com/media/FkIIFHjXEAIBQ33.jpg) ([View Tweet](https://twitter.com/rileytomasek/status/1603854649295085568))
	- The "Ask" functionality does a search for your question and then answers based on the most relevant results. This way, you get Dr. Huberman's answers to your questions, not just what [[GPT-3]] thinks.
	  
	  https://t.co/YC5QosGn4N 
	  
	  ![](https://pbs.twimg.com/media/FkIIYAwXEBsFi9i.jpg) ([View Tweet](https://twitter.com/rileytomasek/status/1603854650872107011))
	- If you search for something that hasn't been covered on The Huberman Lab, it will say the question can't be answered instead of making something up.
	  
	  https://t.co/JIeyrOJkcX 
	  
	  ![](https://pbs.twimg.com/media/FkIIlGXXoAAMkfw.png) ([View Tweet](https://twitter.com/rileytomasek/status/1603854652323336216))
	- How does it work? Transcriptions are generated using Whisper and then embedded using the latest @openai text-embedding-ada-002 model.
	  
	  The vectors are then stored in a @pinecone vector database. A user's query is embedded and then used to find similar vectors in the database. ([View Tweet](https://twitter.com/rileytomasek/status/1603854653871034380))
	- The "Ask" answer uses text-davinci-003 to answer the question given the search results, with instructions not to make stuff up. ([View Tweet](https://twitter.com/rileytomasek/status/1603854656156811264))
	- And the app is @remix_run hosted on @vercel. ([View Tweet](https://twitter.com/rileytomasek/status/1603867732432281617))