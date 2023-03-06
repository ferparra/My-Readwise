title:: The Decoding Algorithms... (highlights)
author:: [[@blennon_ on Twitter]]
full-title:: "The Decoding Algorithms..."
category:: #tweets
url:: https://twitter.com/blennon_/status/1631726427161919489

- Highlights first synced by [[Readwise]] [[Mar 6th, 2023]]
	- The decoding algorithms for LLMs today are rather primitive in that they only predict one word at a time and can get "committed" to a bad completion, e.g. hallucinate, bad reasoning, etc. The brain -- as predicted by Confabulation Theory -- predicts and decodes hierarchically. https://t.co/G4dIY6FK3w ([View Tweet](https://twitter.com/blennon_/status/1631726427161919489))
		- **Note**: Thread
	- I'm excited for the next generation of LLMs with improved prediction and decoding strategies. Hecht-Nielsen's Confabulation Theory predicts this. https://t.co/f0lf3n7J8u 
	  
	  ![](https://pbs.twimg.com/media/FqUNfVoaIAATzuh.jpg) ([View Tweet](https://twitter.com/blennon_/status/1631726428596338688))
	- At each moment, LLMs should predict candidate sets of tokens for multiple positions ahead. These candidates converge into a mutually consistent single token for each position. This means predictions for the next word are also influenced by predictions for 2nd, 3rd, 4th word etc. 
	  
	  ![](https://pbs.twimg.com/media/FqUOdlpaAAATwu2.jpg) ([View Tweet](https://twitter.com/blennon_/status/1631726432471887872))
	- Note: the authors of this great paper fine tuned GPT2 with a long range and high level objective to more closely match the brain imaging results. See Fig 5 and the Methods. ([View Tweet](https://twitter.com/blennon_/status/1631735772247392256))