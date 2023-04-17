title:: How does a Large Language Model like ChatGPT actually work? (highlights)
author:: [[Dan Hollick 🇿🇦]]
full-title:: "How does a Large Language Model like ChatGPT actually work?"
category:: #articles
url:: https://twitter.com/DanHollick/status/1646509271843225600
document_note:: 1. What are some advantages of using a transformer network for natural language processing?
2. How does attention help capture the context of a sentence?
3. What mathematical techniques are used to adjust the weights in a feed forward neural network?

The Large Language Model ChatGPT calculates probabilities of an output based on an input provided by a neural network structure. The network first encodes input words into embeddings, which are fed into an attention process that adds even more context to the embeddings. The process of attention re-weights the embedding based on the context of the sentence to capture the meaning of words with multiple meanings. The contextualized embeddings are then passed through a neural net to produce probabilities. This process unlocks potential and is a simplified version of how an LLM works.
tags:: #[[neural networks]]

- Highlights first synced by [[Readwise]] [[Apr 16th, 2023]]
	- ![](https://pbs.twimg.com/media/FtmTdmJaMAAu0E-.jpg) ([View Highlight](https://read.readwise.io/read/01gy3t2d273gvvg5v6bxsd9khz))
		- **Tags**: #[[llms]]
	- We would need a neural net like this:
	- ![](https://pbs.twimg.com/media/FtmTgVvaYAU8lDc.png) ([View Highlight](https://read.readwise.io/read/01gy3t3a1g2f0mk8e64e6qm4v0))
		- **Tags**: #[[neural networks]]
	- ![](https://pbs.twimg.com/media/FtmTgypakAErT7E.png) ([View Highlight](https://read.readwise.io/read/01gy3t316gve7gwbm7db0hxktp))
		- **Tags**: #[[gpt]] #[[neural networks]]
	- ![](https://pbs.twimg.com/media/FtmThVWaEAAYQlD.jpg) ([View Highlight](https://read.readwise.io/read/01gy3t3v55srs0xe2ssna96nhd))
		- **Tags**: #[[neural networks]]
	- ![](https://pbs.twimg.com/media/FtmTh4naEAIFV4v.jpg) ([View Highlight](https://read.readwise.io/read/01gy3t404f2vs6dzr0phq20rf1))
		- **Tags**: #[[neural networks]]
	- ![](https://pbs.twimg.com/media/FtmTryCacAA-Jv5.png) ([View Highlight](https://read.readwise.io/read/01gy3t48gnsgmdssvqsjxcmt7a))
		- **Tags**: #[[transformers]]
	- Embeddings help create relationships between similar words but they also capture analogies. ([View Highlight](https://read.readwise.io/read/01gy3t56g1q1sxj1tr4d7eke0r))
		- **Tags**: #[[embeddings]]
	- ![](https://pbs.twimg.com/media/FtmTwtbaQAMOtKQ.png) ([View Highlight](https://read.readwise.io/read/01gy3t5rznvxf7z7vctraqdgpv))
		- **Tags**: #[[embeddings]]
		- **Note**: ChatGPT is a Large Language Model that calculates the probabilities of an output based on some input.It uses a neural network structure, where numbers are fed into one side and probabilities are spat out the other.It uses a feed forward neural net with a transformer structure, which breaks words down into tokens that are then represented as a number.This is aided by embeddings, which indicate the word's relationship to other tokens, and attention, which looks back at the sentence for context.The contextualised embeddings are then passed into a neural net to produce probabilities.
	- This attention process happens many times over to capture the context of the sentence in multiple dimensions. ([View Highlight](https://read.readwise.io/read/01gy3t4xfqafg9w6rn3p66xjkm))