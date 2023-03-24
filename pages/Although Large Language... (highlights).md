title:: Although Large Language... (highlights)
author:: [[@cwolferesearch on Twitter]]
full-title:: "Although Large Language..."
category:: #tweets
url:: https://twitter.com/cwolferesearch/status/1635693551584522256

- Highlights first synced by [[Readwise]] [[Mar 16th, 2023]]
	- Although large language models (LLMs) are incredibly capable, they are pretty simple to understand. In fact, the core components of most LLMs can be distilled into five major components… 🧵[1/7] 
	  
	  ![](https://pbs.twimg.com/media/FrMmcbXXsAMG6f9.jpg) ([View Tweet](https://twitter.com/cwolferesearch/status/1635693551584522256))
		- **Note**: Thread
	- 1. The architecture
	  
	  Modern LLMs use decoder-only transformer architectures. Each block of this architecture contains masked self-attention and a feed-forward neural network (single hidden layer). We add layer normalization and residual connections between these layers. [2/7] 
	  
	  ![](https://pbs.twimg.com/media/FrMieXbWwAAjjnK.jpg) ([View Tweet](https://twitter.com/cwolferesearch/status/1635693553035640832))
	- 2. Pre-training procedure
	  
	  Before being used for downstream tasks, LLMs are pre-trained over a big corpus of unlabeled text data. The objective used for pre-training is a language modeling objective, which simply teaches the LLM to accurately predict the next word/token. [3/7] 
	  
	  ![](https://pbs.twimg.com/media/FrMisy-XsBArlJa.jpg) ([View Tweet](https://twitter.com/cwolferesearch/status/1635693554558283797))
	- 3. Downstream adaptation
	  
	  After pre-training, LLMs can accurately predict the next token in a textual sequence. But, how do we use this model to solve tasks like classification or summarization? We have two main options:
	- 4. Making LLMs better
	  
	  The generic framework we’ve described so far has a missing component: scale. To create high-quality LLMs, we need to make them larger. But, scaling up the model only is not enough. We need both a larger model and more pre-training data. [5/7] 
	  
	  ![](https://pbs.twimg.com/media/FrMjWIyWAAEST-h.jpg) ([View Tweet](https://twitter.com/cwolferesearch/status/1635693557536239619))
	- 5. Alignment and specialization
	  
	  Foundation models like GPT-3 are great, but they:
	- For more info on language modeling, check out my series of overviews on the topic: