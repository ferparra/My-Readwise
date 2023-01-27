title:: Building on Parts 1 &Amp... (highlights)
author:: [[@MishaLaskin on Twitter]]
full-title:: "Building on Parts 1 &Amp..."
category:: #tweets
url:: https://twitter.com/MishaLaskin/status/1483584738799624197

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Building on parts 1 & 2 which explained multi-head attention and GPT, in part 3 of the Transformer Series we'll cover masked language models like BERT. 
	  
	  This thread → masked language models, diff between causal and bi-directional masked attention, finetuning, and code.
	  
	  1/N 
	  
	  ![](https://pbs.twimg.com/media/FJbAdMeWUAYiEPN.jpg) ([View Tweet](https://twitter.com/MishaLaskin/status/1483584738799624197))
		- **Note**: Thread
	- Since we'll be referencing multi-head attention and GPT, make sure to read parts 1 & 2 if you're unfamiliar with these concepts.
	  
	  Part 2, GPT:  https://t.co/5KgMtVVgFU
	  Part 1, Multi-head attention: https://t.co/Hwlnmk1OAB
	  
	  2/N ([View Tweet](https://twitter.com/MishaLaskin/status/1483584740125032450))
	- We saw with GPT that we can pre-train language models with a causal predict-the-future objective. Instead, BERT uses a fill-in-the-blank objective. It is called bi-directional because unlike GPT (which is causal) it sees both past and future tokens at once.
	  
	  3/N 
	  
	  ![](https://pbs.twimg.com/media/FJbAdlzXoAU6Fut.jpg) ([View Tweet](https://twitter.com/MishaLaskin/status/1483584745145520129))
	- So how does BERT work? The architecture is outlined below. BERT works (almost) exactly like GPT except for two main differences: (A) instead of using a causal mask we use a random one (B) BERT prepends an additional [CLS] to each sequence. What is this new [CLS] token? 
	  
	  4/N 
	  
	  ![](https://pbs.twimg.com/media/FJbAd5tXIAQoJG8.jpg) ([View Tweet](https://twitter.com/MishaLaskin/status/1483584750514282497))
	- Suppose we want to use BERT for sentiment classification. Our transformer's outputs have shape (B, T, D). We want to compress this to (B, D) so each data pt has an aggregate representation that we can feed into a classifier. First guess - how about we average over the T dim?
	  
	  5/N ([View Tweet](https://twitter.com/MishaLaskin/status/1483584752041005060))
	- This will work, but it assumes that all tokens are equally useful for classification. Isn't the whole point of attention to weigh tokens based on their relevance? What if we add a new token to the input that aggregates the other tokens with attention? That's the pt of [CLS].
	  
	  6/N 
	  
	  ![](https://pbs.twimg.com/media/FJbAeQbWQAAItl8.jpg) ([View Tweet](https://twitter.com/MishaLaskin/status/1483584756583444485))
	- When we finetune BERT for classification (hence name of token), we use the final hidden state of the [CLS] token as the input to a classifier, which is just an MLP that projects the [CLS] hidden state with shape (B,D) to the number of classes with shape (B, num_classes). 
	  
	  7/N ([View Tweet](https://twitter.com/MishaLaskin/status/1483584757988474880))
	- Aside from [CLS] there are other special tokens in BERT - namely [MASK], which replaces masked tokens, and [SEP] which is a sentence separation token. Tokenization happens during data loading. Once we've tokenized, we fuse these and positional tokens like in the code below.
	  
	  8/N 
	  
	  ![](https://pbs.twimg.com/media/FJbAem8XMAEOp5Y.jpg) ([View Tweet](https://twitter.com/MishaLaskin/status/1483584762476482563))
	- Now that we know how tokenization works, the BERT block and pre-training objectives are actually identical to GPT. The only diff is that BERT uses a random mask while GPT uses a causal one, but the code implementation is nearly identical for both.
	  
	  8/N 
	  
	  ![](https://pbs.twimg.com/media/FJbAe5XXwAAcyDm.jpg) ([View Tweet](https://twitter.com/MishaLaskin/status/1483584768000376838))
	- For BERT, each time we pass in a batch of data for [[pre-training]], we sample a new random mask. This can be done efficiently if the mask is created directly on the GPU. Here's what what mask creation and masked [[language modeling]] objective look like. Pretty straightforward!
	  
	  9/N 
	  
	  ![](https://pbs.twimg.com/media/FJbAfNyXIAQilN2.jpg) ([View Tweet](https://twitter.com/MishaLaskin/status/1483584773746577408))
	- Tl;dr BERT = GPT but with random masking and some special tokens (e.g. [CLS] token). It's remarkable that transformers are so simple and general-purpose.
	  
	  Next time I'll show how transformers can be used in computer vision with the Vision Transformer (ViT) + MAE loss. 
	  
	  10/N END ([View Tweet](https://twitter.com/MishaLaskin/status/1483584775009021953))