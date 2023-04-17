title:: How do you measure the query performance/hallucination on @gpt_index *without*... (highlights)
author:: [[Jerry Liu]]
full-title:: "How do you measure the query performance/hallucination on @gpt_index *without*..."
category:: #articles
url:: https://twitter.com/jerryjliu0/status/1641234014991446016

- Highlights first synced by [[Readwise]] [[Apr 7th, 2023]]
	- ![](https://pbs.twimg.com/media/FsbVoyqaUAAqoTO.jpg) ([View Highlight](https://read.readwise.io/read/01gx9svtf6r09x6s05p60dq9g5))
		- **Note**: This document explains how to measure the query performance and hallucination on @gpt_index without ground-truth labels. A new evaluation module allows users to compare the synthesized text response with the retrieved sources. The evaluation module stores the sources in a list index data structure, and checks if the synthesized response matches the sources. Examples are provided to demonstrate the effectiveness of the evaluation module. Finally, a link to a full notebook is provided.