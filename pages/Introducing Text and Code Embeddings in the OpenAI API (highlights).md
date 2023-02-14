title:: Introducing Text and Code Embeddings in the OpenAI API (highlights)
author:: [[OpenAI]]
full-title:: "Introducing Text and Code Embeddings in the OpenAI API"
category:: #articles
url:: https://openai.com/blog/introducing-text-and-code-embeddings/

- Highlights first synced by [[Readwise]] [[Feb 11th, 2023]]
	- Embeddings are numerical representations of concepts converted to number sequences, which make it easy for computers to understand the relationships between those concepts. ([View Highlight](https://read.readwise.io/read/01grwy7brqf9xkq8grydwfwft6))
		- **Tags**: #[[embeddings]]
	- Text similarity models provide embeddings that capture the semantic similarity of pieces of text. These models are useful for many tasks including [clustering](https://beta.openai.com/docs/guides/embeddings/clustering), [data visualization](https://beta.openai.com/docs/guides/embeddings/data-visualization-in-2d), and [classification](https://beta.openai.com/docs/guides/embeddings/classification-using-the-embedding-features). ([View Highlight](https://read.readwise.io/read/01grwy70cj9knb8cf92jqgkj05))
	- To compare the similarity of two pieces of text, you simply use the [dot product](https://en.wikipedia.org/wiki/Dot_product) on the text embeddings. The result is a “similarity score”, sometimes called “[cosine similarity](https://en.wikipedia.org/wiki/Dot_product#Application_to_the_law_of_cosines),” between –1 and 1, where a higher number means more similarity. ([View Highlight](https://read.readwise.io/read/01grwy6pa4gmye0fqtwrrxjtn1))
	- Code search models provide code and text embeddings for code search tasks. Given a collection of code blocks, the task is to find the relevant code block for a natural language query. ([View Highlight](https://read.readwise.io/read/01grwy6860vp4s92y0rp8fsk9k))
	- [FineTune Learning](https://finetunelearning.com/) is a company building hybrid human-AI solutions for learning, like [adaptive learning loops](https://en.wikipedia.org/wiki/Adaptive_learning) that help students reach academic standards.
	  
	  OpenAI’s embeddings significantly improved the task of finding textbook content based on learning objectives ([View Highlight](https://read.readwise.io/read/01grwy5t546rda6dnmwn00p4zy))