title:: The Solution to TL;DRs - Weaviate's Summarizer Module (highlights)
author:: [[weaviate.io]]
full-title:: "The Solution to TL;DRs - Weaviate's Summarizer Module"
category:: #articles
url:: https://weaviate.io/blog/solution-to-tl-drs

- Highlights first synced by [[Readwise]] [[Apr 7th, 2023]]
	- For a while now, the bottleneck in knowledge work has been our rate of information discovery and consumption. So how do we solve this problem?
	  
	  You probably already know that Weaviate, as a vector database, can help with information cataloging and discovery. But did you know that Weaviate can also summarize information during retrieval?
	  
	  Our summarizer module ([`sum-transformers`](https://weaviate.io/developers/weaviate/modules/reader-generator-modules/sum-transformers)) can be added to a Weaviate instance to do exactly that.
	  
	  And as a bonus, we will also show you how to use our new generative module (`generative-openai`) to do the same thing as well. ([View Highlight](https://read.readwise.io/read/01gx9s9evatgcn1f959tmgkkn1))
	- The summarization module achieves this at query time by passing on the text that is retrieved from Weaviate to a language model that is trained specifically for summarization. ([View Highlight](https://read.readwise.io/read/01gx9sacezbhkp8jwgcq481b27))
	- ![Summarized documents are easier to understand](https://weaviate.io/assets/images/weaviate-summarize-dark-6c29742594b27bf9395e22654b2a690b.png#gh-dark-mode-only) ([View Highlight](https://read.readwise.io/read/01gx9sagrvw3r66xhn46amdter))
	- All transformer models have a maximum input length size. For example, `bart-large-cnn` has a maximum limit of 1024 tokens, where each token is part of a word (i.e. a few characters).
	  
	  Inputting too long a text into the summarizer module will cause it to throw an error. Accordingly, if you envisage generating summaries using `sum-transformers`, we recommend considering chunking your data at import time to make sure that the content of each field is shorter than the maximum length. ([View Highlight](https://read.readwise.io/read/01gx9sbbmfb6dawv7v9t9rw7gq))
	- The [Goldilocks Principle](https://en.wikipedia.org/wiki/Goldilocks_principle) also applies here, where too short an input may cause the summarizer model to misbehave (i.e. [hallucinate](https://en.wikipedia.org/wiki/Hallucination_(artificial_intelligence))).
	  
	  When fed insufficient input, the model may "pad" the output with tokens that have very little grounding in the truth. Generally speaking, an input length that is shorter than a typical "summary" output length by the model is inadvisable. ([View Highlight](https://read.readwise.io/read/01gx9sbh5ftdfqm26f32fsezkr))
	- Bonus: TL;DR version (edited):[​](https://weaviate.io/blog/solution-to-tl-drs#bonus-tldr-version-edited)
	  
	  Weaviate can also summarize information during retrieval through the use of its summarizer module, `sum-transformers`.
	  
	  This module can shorten a piece of text into a pithy, to-the-point summary by passing the text retrieved from Weaviate to a language model trained specifically for summarization.
	  
	  By using Weaviate to summarize your data, you can reduce the amount of too long; did not read (TL;DR) content in your life and reduce the problem of information overload. The `sum-transformers` module uses the `bart-large-cnn` model by default, with an option for the `pegasus-xsum` model, but any model from Hugging Face Hub can be used. ([View Highlight](https://read.readwise.io/read/01gx9sbrf7ppa2dh6mg56dwjav))