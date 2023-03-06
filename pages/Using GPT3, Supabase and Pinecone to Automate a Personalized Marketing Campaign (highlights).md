title:: Using GPT3, Supabase and Pinecone to Automate a Personalized Marketing Campaign (highlights)
author:: [[ycombinator.com]]
full-title:: "Using GPT3, Supabase and Pinecone to Automate a Personalized Marketing Campaign"
category:: #articles
url:: https://news.ycombinator.com/item?id=34939053

- Highlights first synced by [[Readwise]] [[Feb 26th, 2023]]
	- > My script read through each of the products we had responses for, called OpenAI's embedding api and loaded it into Pinecone - with a reference to the Supabase response entry.
	  
	  OpenAI and the Pinecone database are not really needed for this task. A simple SBERT encoding of the product texts, followed by storing the vectors in a dense numpy array or faiss index would be more than sufficient. Especially if one is operating in batch mode, the locality and simplicity can’t be beat and you can easily scale to 100k-1M texts in your corpus on commodity hardware/VPS (though NVME disk will see a nice performance gain over regular SSD) ([View Highlight](https://read.readwise.io/read/01gt64shspavkr4y0hs7e4eafm))