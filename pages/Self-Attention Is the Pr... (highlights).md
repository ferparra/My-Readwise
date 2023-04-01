title:: Self-Attention Is the Pr... (highlights)
author:: [[@cwolferesearch on Twitter]]
full-title:: "Self-Attention Is the Pr..."
category:: #tweets
url:: https://twitter.com/cwolferesearch/status/1641932082283700226

- Highlights first synced by [[Readwise]] [[Apr 1st, 2023]]
	- Self-attention is the primary building block of large language models (LLMs) and transformers in general. But, how exactly does it work? 🧵 [1/8] 
	  
	  ![](https://pbs.twimg.com/media/FslQGUeWwAM6Q7U.jpg) ([View Tweet](https://twitter.com/cwolferesearch/status/1641932082283700226))
		- **Note**: Thread
	- The input to a self-attention mechanism is an ordered list of vectors. Each of these vectors represents a token within an underlying sequence. In language applications, these tokens roughly correspond to words (or subwords) in a sentence. [2/8] 
	  
	  ![](https://pbs.twimg.com/media/FslNaVyX0AAAZZA.jpg) ([View Tweet](https://twitter.com/cwolferesearch/status/1641932084246720512))
	- Given this list of ordered vectors, self-attention computes a new vector for each token within the sequence. Put simply, each token’s new vector is computed as a weighted average of all other vectors within the sequence. [3/8] 
	  
	  ![](https://pbs.twimg.com/media/FslNjvFWwAIbMjG.jpg) ([View Tweet](https://twitter.com/cwolferesearch/status/1641932086327013376))
	- However, we don’t actually compute weighted averages of the vectors themselves! We first pass all of the vectors in the sequence through a (learnable) linear projection to produce “value” vectors, then take a weighted average of these value vectors. [4/8] 
	  
	  ![](https://pbs.twimg.com/media/FslN4pVWAAAbt7U.jpg) ([View Tweet](https://twitter.com/cwolferesearch/status/1641932087887290372))
	- The final question is: how do we compute the attention weights used in the weighted average?
	  
	  First, we pass all token vectors through two separate linear projections (just like for the value vectors) to produce the “key” and “query” vectors. [5/8] 
	  
	  ![](https://pbs.twimg.com/media/FslOG9jX0AI58OE.jpg) ([View Tweet](https://twitter.com/cwolferesearch/status/1641932090093494273))
	- Now, let’s assume we are computing the output vector for the i-th token. The attention weight between token i and another token j is just given by the inner product of the i-th query vector and the j-th key vector! [6/8] 
	  
	  ![](https://pbs.twimg.com/media/FslORWrWYAIyIBK.jpg) ([View Tweet](https://twitter.com/cwolferesearch/status/1641932093000130561))
	- The only remaining complication here is that we take a softmax over attention weights so that all attention weights for each token sum to one. The weighted average is performed for all tokens in the sequence. We can “vectorize” this operation as shown below. [7/8] 
	  
	  ![](https://pbs.twimg.com/media/FslOfcDWIAA9Yqn.jpg) ([View Tweet](https://twitter.com/cwolferesearch/status/1641932095051247616))
	- Here are some more links for better understanding self-attention: