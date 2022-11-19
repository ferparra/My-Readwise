title:: Techniques for Training Large Neural Networks (highlights)
author:: [[openai.com]]
full-title:: "Techniques for Training Large Neural Networks"
category:: #articles
url:: https://openai.com/blog/techniques-for-training-large-neural-networks/

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Data Parallel training means copying the same parameters to multiple GPUs (often called “workers”) and assigning different examples to each to be processed simultaneously.
	- As each data parallel worker updates its copy of the parameters, they need to coordinate to ensure that each worker continues to have similar parameters.