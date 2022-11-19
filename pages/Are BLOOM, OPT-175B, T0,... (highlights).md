title:: Are BLOOM, OPT-175B, T0,... (highlights)
author:: [[@dtredsox13 on Twitter]]
full-title:: "Are BLOOM, OPT-175B, T0,..."
category:: #tweets
url:: https://twitter.com/dtredsox13/status/1592980027028967424

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Are BLOOM, OPT-175B, T0, and GPT-NeoX "factually consistent"? 
	  
	  New preprint! We introduce FIB - the Factual Inconsistency Benchmark - and evaluate 23 LLMs. 
	  
	  Work done with @anisham197 @byryuer @mohitban47 @colinraffel
	  
	  📄 https://t.co/ytR0HAPRwJ
	  💾 https://t.co/MytSc3S17M
	  🧵 ⬇️ 
	  
	  ![](https://pbs.twimg.com/media/Fhtk54IXkAABZQr.jpg) ([View Tweet](https://twitter.com/dtredsox13/status/1592980027028967424))
		- **Note**: Thread
	- In FIB, models are given a document and evaluated on whether they prefer a factually consistent summary over a factually inconsistent summary. A model’s preference for a summary is computed using the length-normalized pointwise mutual information. (2/8) ([View Tweet](https://twitter.com/dtredsox13/status/1592980030493458432))
	- All the summaries in FIB were manually verified as factually consistent or factually inconsistent. Factually inconsistent summaries were generated from models trained for summarization and annotated as factually inconsistent. (3/8) ([View Tweet](https://twitter.com/dtredsox13/status/1592980032212717568))
	- We find that BLOOM, OPT-175B, and other zero-shot LLMs often prefer factually consistent summaries to factually inconsistent summaries on XSum. Also, LLMs are slightly more factually consistent as they are scaled up. (4/8) 
	  
	  ![](https://pbs.twimg.com/media/FhtlmV_XkAQkI50.jpg) ([View Tweet](https://twitter.com/dtredsox13/status/1592980036411600898))
	- However, when the summaries are extracted from the document for CNN/DM,  we find the models heavily prefer the extracted summaries, regardless of its factuality. (5/8) 
	  
	  ![](https://pbs.twimg.com/media/FhtlqNoWYAI_9C5.jpg) ([View Tweet](https://twitter.com/dtredsox13/status/1592980040748216320))
	- We also experiment with using other factually inconsistent distractor methods including FactCC (https://t.co/PitjsGPINT). On XSum, FactCC can fool zero-shot LLMs at roughly the same rate as FIB, but this does not hold across all architectures and models. (6/8) 
	  
	  ![](https://pbs.twimg.com/media/FhtjjtKXwAA23bu.jpg) ([View Tweet](https://twitter.com/dtredsox13/status/1592980046255247360))
	- Finally, we test different scoring functions that the model uses to assign scores to a summary, and find that average pointwise mutual information works best for summaries not extracted from the document. (7/8) 
	  
	  ![](https://pbs.twimg.com/media/Fhtm1R0XgAEg3Ve.jpg) ([View Tweet](https://twitter.com/dtredsox13/status/1592980051641143296))