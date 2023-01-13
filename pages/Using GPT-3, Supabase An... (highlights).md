title:: Using [[GPT-3]], Supabase An... (highlights)
author:: [[@vimota on Twitter]]
full-title:: "Using GPT-3, Supabase An..."
category:: #tweets
url:: https://twitter.com/vimota/status/1581444899299131392

- Highlights first synced by [[Readwise]] [[Dec 20th, 2022]]
	- Using [[GPT-3]], Supabase and Pinecone, I built a semantic embeddings search that saved hundreds of hours of manual work for my girlfriends skincare brand (https://t.co/vj4K2sGMLm).
	  
	  It actually worked much better than I expected - this is how I did it: ([View Tweet](https://twitter.com/vimota/status/1581444899299131392))
		- **Note**: Thread
	- First some context. @mariaaacasa started Oliver Care with the goal of creating a brand that educates people on the risks of Endocrine Disrupting Chemicals (EDCs) in every day items and formulates EDC-free products. ([View Tweet](https://twitter.com/vimota/status/1581444901891284992))
	- She had the idea of doing a personalized EDC report where anyone could send their daily routines and she'd look at each item and identify which contained EDCs and make suggestions.
	  
	  At first she'd get a couple a day, from her TikTok following, but that quickly grew to thousands😳 
	  
	  ![](https://pbs.twimg.com/media/FfJrw2OVUAA0wsz.jpg) ([View Tweet](https://twitter.com/vimota/status/1581444911039008768))
	- At that point, we realized she'd have to automate it somehow.
	  
	  We had all the email addresses and their submitted routines in Klaviyo which I exported to Supabase. I got her to put down the most popular products she had already seen and her response to each and loaded as well. 
	  
	  ![](https://pbs.twimg.com/media/FfJrxPVVEAAbeE2.jpg) ([View Tweet](https://twitter.com/vimota/status/1581444917535965184))
	- I was hoping I'd be able to write a quick script to do some regex parsing and use the `pg_trgm` extension on @supabase to look up each product in a person's routine and match it to a product responses she'd filled in. ([View Tweet](https://twitter.com/vimota/status/1581444920467857408))
	- That worked exactly as expected - text search is actually super easy with Postgres.
	  
	  ... But text search isn't really enough. People would send in product names formatted in all types of ways. And there's multiple names for the same product. Text search isn't really well suited. ([View Tweet](https://twitter.com/vimota/status/1581444923055738880))
	- Next I thought, maybe [[GPT-3]] could automate this completely.
	  
	  And it pretty much worked! Using prompts to find matches is not really ideal, but we want to use GPT's semantic understanding.
	  
	  That's where Embeddings come in. 
	  
	  ![](https://pbs.twimg.com/media/FfJrx7FVsAAiAHm.png) 
	  
	  ![](https://pbs.twimg.com/media/FfJryJiUcAAe0Gu.png) ([View Tweet](https://twitter.com/vimota/status/1581444932778176512))
	- Embeddings are the dense vector representation of an input encoded by the model, how the model represents a concept.
	  
	  Since embeddings are just vectors, you can calculate distances between them which represent how conceptually similar they are from each other. 
	  
	  ![](https://pbs.twimg.com/media/FfJrygHUcAARPLs.jpg) ([View Tweet](https://twitter.com/vimota/status/1581444939220541441))
	- @openai exposes embeddings calculation for each of their [[GPT-3]] models as an API. But you still need to do the vector distance calculation yourself.
	  
	  You can do it in code, iterating through all the potential matches and calculating the cosine distance, or you can use a vector DB. ([View Tweet](https://twitter.com/vimota/status/1581444942253080576))
	- I thought I'd try out @pinecone which is built for this exact purpose. My script read through each of the products we had responses for, called OpenAI's embedding api and loaded it into Pinecone - with a reference to the Supabase response entry. ([View Tweet](https://twitter.com/vimota/status/1581444944807370753))
	- Once the response lookups were loaded into Pinecone, the script could query it for the most similar match for each item in someone's routine and pre-populate the response for their submission. ([View Tweet](https://twitter.com/vimota/status/1581444947307204608))
	- From there we just had to run it for the thousands of submissions, export the results as a custom property of each Klaviyo user profile and kick off a campaign to email them their results.
	  
	  Just like that, 100s of human hours saved using [[GPT-3]] and Pinecone 🔥 ([View Tweet](https://twitter.com/vimota/status/1581444949865680896))
	- People normally focus on [[GPT-3]]'s generative ability to produce content, but using it for this made me realize how many use cases could take advantage of it's semantic understanding of concepts. ([View Tweet](https://twitter.com/vimota/status/1581444952466153473))
	- One thing I'd love to play around with is extracting dimensions of an embedding, ie. for "cerave moisturizer", being able to calculate the "product" (moisturizer) distance to something vs the "brand" (cerave) distance. ([View Tweet](https://twitter.com/vimota/status/1581444955091804160))
	- While you're here, if you care about protecting your hormone health check out Oliver Care :) https://t.co/vj4K2sGMLm ([View Tweet](https://twitter.com/vimota/status/1581445255026515969))
	- Exactly this: https://t.co/vkFzZA8lTT ([View Tweet](https://twitter.com/vimota/status/1584939837660200962))