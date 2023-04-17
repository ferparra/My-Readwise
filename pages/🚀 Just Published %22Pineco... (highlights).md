title:: 🚀 Just Published "Pineco... (highlights)
author:: [[@nextworddev on Twitter]]
full-title:: "🚀 Just Published "Pineco..."
category:: #tweets
url:: https://twitter.com/nextworddev/status/1644089351918198784

- Highlights first synced by [[Readwise]] [[Apr 7th, 2023]]
	- 🚀 Just published "Pinecone DB - Cost Optimization & Performance Best Practices"! @pinecone 
	  
	  🧠 Dive into 17 actionable tips that could save you thousands of dollars or prevent surprise bills for your #AI or @LangChainAI  projects.
	  
	  🌲 Here's a summary thread👇 
	  
	  ![](https://pbs.twimg.com/media/FtD6XnyXoAE6Juv.jpg) ([View Tweet](https://twitter.com/nextworddev/status/1644089351918198784))
		- **Note**: Thread
	- @pinecone @LangChainAI 💳 First and foremost, decide if you require a paid plan. A single S-type pod can store 2million 1536 dimension vectors. Most projects don't have >300K embeddings. Only upgrade when you go beyond that, or have some strict SLAs due to production use. ([View Tweet](https://twitter.com/nextworddev/status/1644089719871897602))
	- 🔐 Namespace Isolation: You can split a single index across multiple apps by using a convention like this. e.g. namespace=[{project_name}_{subnamespace}] to separate and query vectors in an isolated manner. Avoid upgrading just for multiple indices. ([View Tweet](https://twitter.com/nextworddev/status/1644090188233072641))
	- 🔄 Leverage collections to save on idle time costs:
	  
	  1. Create snapshots of your index as collections
	  2. Delete your index when idle
	  3. Rehydrate index from collections when needed
	  4. Don't fear deleting indices; they're not for data storage 
	  
	  ![](https://pbs.twimg.com/media/FtD7N38XwAEuqNX.jpg) ([View Tweet](https://twitter.com/nextworddev/status/1644090189487427584))
	- 💼 Sharing my experience from AWS, Alexa, and using Pinecone in production. I've helped hundreds of customers architect production #ML systems. Follow this thread for practical tips on Pinecone cost optimization! 🌟 ([View Tweet](https://twitter.com/nextworddev/status/1644090191068495873))
	- 📦 Treat Pinecone as a vector DB, not NoSQL:
	  
	  Avoid storing entire JSON objects as metadata
	  Store just foreign_key or uuid in metadata, linking to actual documents in another datastore ([View Tweet](https://twitter.com/nextworddev/status/1644090599027384320))
	- Leverage a script to dynamically scale-in and scale-out your Pinecone cluster. More on that here. https://t.co/LmwCuDGtNC 
	  
	  ![](https://pbs.twimg.com/media/FtD7nlDWAAAcTQW.jpg) ([View Tweet](https://twitter.com/nextworddev/status/1644090600193507329))
	- 🚀 Use replicas to boost performance:
	  
	  1. Add replicas when experiencing degraded query performance
	  2/ Replicas distribute the load and increase throughput
	  Note: Replicas won't increase vector storage capacity ([View Tweet](https://twitter.com/nextworddev/status/1644090601514598405))
	- 🚧 When prototyping, use storage-optimized S type pods instead of P1 or P2 for better storage capacity and cost efficiency. ([View Tweet](https://twitter.com/nextworddev/status/1644090602659651584))
	- 🎯 In summary, optimize Pinecone costs by understanding its features, choosing the right pods, structuring your data efficiently, and leveraging collections & replicas wisely. 
	  
	  Happy cost-saving! 🎉 ([View Tweet](https://twitter.com/nextworddev/status/1644090603951763462))