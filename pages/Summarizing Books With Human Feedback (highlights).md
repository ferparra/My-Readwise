title:: Summarizing Books With Human Feedback (highlights)
author:: [[openai.com]]
full-title:: "Summarizing Books With Human Feedback"
category:: #articles
url:: https://openai.com/research/summarizing-books
tags:: #[[gpt-3]]

- Highlights first synced by [[Readwise]] [[Mar 20th, 2023]]
	- Consider the task of summarizing a piece of text. Large [pretrained models aren’t very good at summarization](https://openai.com/blog/learning-to-summarize-with-human-feedback/). In the past we found that training a model with [reinforcement learning from human feedback](https://openai.com/blog/deep-reinforcement-learning-from-human-preferences/) helped align model summaries with human preferences on short posts and articles. But judging summaries of entire books takes a lot of effort to do directly since a human would need to read the entire book, which takes many hours.
	  
	  To address this problem, we additionally make use of *recursive task decomposition*: we procedurally break up a difficult task into easier ones. In this case we break up summarizing a long piece of text into summarizing several shorter pieces. Compared to an end-to-end training procedure, recursive task decomposition has the following advantages:
	  
	  1.  Decomposition allows humans to evaluate model summaries more quickly by using summaries of smaller parts of the book rather than reading the source text.
	  2.  It is easier to trace the summary-writing process. For example, you can trace to find where in the original text certain events from the summary happen. See for yourself on [our summary explorer](https://openaipublic.blob.core.windows.net/recursive-book-summ/website/index.html)!
	  3.  Our method can be used to summarize books of unbounded length, unrestricted by the context length of the transformer models we use. ([View Highlight](https://read.readwise.io/read/01gvyqxd2pyxd0kdcfr546718t))