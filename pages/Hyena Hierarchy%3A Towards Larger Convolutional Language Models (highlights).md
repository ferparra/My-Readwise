title:: Hyena Hierarchy: Towards Larger Convolutional Language Models (highlights)
author:: [[Stanford Report]]
full-title:: "Hyena Hierarchy: Towards Larger Convolutional Language Models"
category:: #articles
url:: https://hazyresearch.stanford.edu/blog/2023-03-07-hyena
tags:: #[[convolutional models]]

- Highlights first synced by [[Readwise]] [[Apr 22nd, 2023]]
	- We're excited to share our latest work on Hyena, a subquadratic-time layer that has the potential to significantly increase context length in sequence models, using a combination of long convolutions and gating. ([View Highlight](https://read.readwise.io/read/01gyk1eks60md1pfe2q509v5bn))
	- Attention is great – it powers many of the most exciting AI models, from ChatGPT to Stable Diffusion. ([View Highlight](https://read.readwise.io/read/01gyk1f0qx88errg9yztwthwxv))
	- Attention is fundamentally a quadratic operation, as it compares each pair of points in a sequence. This quadratic runtime has limited the amount of context that our models can take. In the approaches we’ll discuss below, we started to think about models that can handle sequences with millions of tokens–orders of magnitude longer than what Transformers can process today. (e.g, imagine feeding ChatGPT a whole textbook as context and reasoning about it in a zero-shot setting, or having as context every keystroke you’ve ever written, or conditioning a patient’s entire health record. Sounds amazing!) ([View Highlight](https://read.readwise.io/read/01gyk1g4ht1yhycw3cy9hkfc9e))
	- ![](https://hazyresearch.stanford.edu/static/posts/2023-03-07-hyena/diagram.png) ([View Highlight](https://read.readwise.io/read/01gyk1mwsg68jbszpr2dsp8qn4))