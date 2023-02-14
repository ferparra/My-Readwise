title:: Man and Machine: GPT for Second Brains (highlights)
author:: [[reasonabledeviations.com]]
full-title:: "Man and Machine: GPT for Second Brains"
category:: #articles
url:: https://reasonabledeviations.com/2023/02/05/gpt-for-second-brain/
document_note:: This article outlines the author's use of GPT embeddings to build a smart search tool for their second-brain note-taking system. They explain the basics of GPT, how to use the text completions API to build their own version of ChatGPT, and how to use the embeddings API to represent text blocks as high dimensional space vectors. They then describe how they used their Python script to embed the notes from their Obsidian vault and wrote a utility function to compute the cost of embedding a list of notes. Finally, they discuss the possibility of using GPT-3 to generate requests for summarizing and highlighting disagreements between notes.

- The author defines embeddings as a way to represent a block of text as a point in a high dimensional space, which allows for useful information to be derived from its location. The author provides examples of how this works, such as "king = queen + man" and "tiger = cat + stripes", and "slower - slow + fast = faster". They also provide an example of an embedding function, which takes in a text block and outputs a vector.
  tags:: #[[gpt]] #[[second brain]] #[[semantic search]]
- Highlights first synced by [[Readwise]] [[Feb 11th, 2023]]
	- As my collection of notes grows, I have recently been running into a retrieval issue: sometimes I’m trying to find an idea I know I’ve written about but I can’t remember the name of the concept or where I came across it. ([View Highlight](https://read.readwise.io/read/01grwx7x6m1tyct1n7hdm9d3an))
		- **Tags**: #[[memory]] #[[information retrieval]]
	- The main task of GPT-3 is text completion ([View Highlight](https://read.readwise.io/read/01grwxa6m34x9zx2h5rnczxs0p))
		- **Tags**: #[[gpt]]
	- The core idea of embeddings is to represent a block of text as a point in space (specifically, a vector in high dimensional space). ([View Highlight](https://read.readwise.io/read/01grwxavqtyr0qhkxsq9pfayb5))
		- **Tags**: #[[embeddings]]
	- We mostly want to do this because once text has some spatial location, we can derive useful information based on its location. For example, we might be able to see that “dog” and “cat” are spatially closer than “dog” and “trumpet”. ([View Highlight](https://read.readwise.io/read/01grwxbh3vkevyd1h5a04p8c45))
	- ![](https://reasonabledeviations.com/assets/images/nmr/word2vec.png) ([View Highlight](https://read.readwise.io/read/01grwxdms2c8m45ptrwyzfkeac))
		- **Tags**: #[[word2vec]] #[[charts]] #[[embeddings]]
	- •   Take a bunch of text blocks and feed them to the OpenAI embeddings API. This returns a 1536-dimensional vector for each text block.
	  •   Likewise, embed the search query using the same API to get a query vector.
	  •   Find the most similar vectors among my notes. There are several options to compute the similarity between vectors, but most people default to cosine distance, which measures how closely two vectors align.
	  •   Return the top n notes by similarity. ([View Highlight](https://read.readwise.io/read/01grwxfdwff52rry7cg0ndwang))
	- ![](https://reasonabledeviations.com/assets/images/nmr/gpt_embedding_explanation.png) ([View Highlight](https://read.readwise.io/read/01grwxfr49a8d1g6r2cg2n2a64))
		- **Tags**: #[[chatgpt]] #[[prompt]]
	- ![](https://reasonabledeviations.com/assets/images/nmr/gpt_code_explanation.png) ([View Highlight](https://read.readwise.io/read/01grwxhbdqf9xazr4nj5s8v4ft))
	- The result of this step is a dictionary representation of my entire Obsidian vault, mapping the note name and chapter to the note text. ([View Highlight](https://read.readwise.io/read/01grwxhx8r7dz6hfq6zamc49sg))