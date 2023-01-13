title:: Anyone Else Trying to Us... (highlights)
author:: [[@colinfortuner on Twitter]]
full-title:: "Anyone Else Trying to Us..."
category:: #tweets
url:: https://twitter.com/colinfortuner/status/1610638593537474561

- Highlights first synced by [[Readwise]] [[Jan 5th, 2023]]
	- Anyone else trying to use EXTERNAL knowledge (databases) in their [[GPT-3]] prompts?
	  
	  e.g. adding ‘context’ to a prompt or chain to generate better results?
	  
	  just saw this paper “Rethinking with Retrieval” which looks promising.
	  https://t.co/MeQEJufBz0
	  
	  A short breakdown: ([View Tweet](https://twitter.com/colinfortuner/status/1610638593537474561))
		- **Note**: Thread
	- TLDR
	  ⁃LLM’s don’t have complete knowledge (yet)
	  ⁃This can lead them to predict wrong answers / invalid facts etc.
	  ⁃So we need a way to tell them about recent events / new data
	  ⁃Combined with CoT/self consistency, this leads to better results!
	  
	  How? ([View Tweet](https://twitter.com/colinfortuner/status/1610640722029588480))
	- By retrieving relevant external data based on the “decomposed reasoning steps” from the CoT prompting. ([View Tweet](https://twitter.com/colinfortuner/status/1610640724785254401))
	- Here’s how they implemented it for one task: 
	  
	  Common sense reasoning ->
	  
	  For each sentence explanation in the CoT output:
	  1. get the top 10 relevant paragraphs from their knowledge base 
	  
	  2. find most similar paragraph to to the sentence
	  
	  3. Score sentence faithfulness ([View Tweet](https://twitter.com/colinfortuner/status/1610643997378084864))
	- (Faithfulness determined by entailment/contradiction scores and similarity of all sentences)
	  
	  4. Make a prediction with “faithful inference” (details in paper) ([View Tweet](https://twitter.com/colinfortuner/status/1610643999206899715))
	- I left out a lot of details and it Seems pretty complex and likely slow to run, but I’m excited to see if anyone can make this work! ([View Tweet](https://twitter.com/colinfortuner/status/1610644001484414977))