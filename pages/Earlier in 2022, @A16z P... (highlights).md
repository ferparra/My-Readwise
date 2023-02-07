title:: Earlier in 2022, @A16z P... (highlights)
author:: [[@jerryjliu0 on Twitter]]
full-title:: "Earlier in 2022, @A16z P..."
category:: #tweets
url:: https://twitter.com/jerryjliu0/status/1611402504671236096

- Highlights first synced by [[Readwise]] [[Feb 4th, 2023]]
	- Earlier in 2022, @a16z put out a great update to “Emerging Architectures for Modern Data Infrastructure,” with architecture diagrams detailing the data/AI landscape.
	  
	  With the rise in LLM’s/generative AI, it’s time to think about another update (a small 🧵): 
	  
	  ![](https://pbs.twimg.com/media/FlzX-oPaEAA9mGV.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1611402504671236096))
		- **Note**: Thread
	- The MLOps landscape will need to adapt to LLMOps. A full treatment of this is better left to an updated @a16z article, but here’s some of my high-level thoughts.
	  
	  (1) Any company building apps on top of pre-trained LLM’s (even without finetuning) will require LLMOps tooling… ([View Tweet](https://twitter.com/jerryjliu0/status/1611402506210545671))
	- …because prompts are the new models. Like models, they have input variables and output variables. Like models, they have parameters (text) that affect the output. Like models, they’re intended for certain tasks.
	  
	  Like models, they need to be tracked, versioned, evaluated. ([View Tweet](https://twitter.com/jerryjliu0/status/1611402507984699393))
	- (2) Evaluation will become even more challenging and important. Measuring the quality of generated outputs is no longer as simple as MSE from sklearn on a single float number. ([View Tweet](https://twitter.com/jerryjliu0/status/1611402509612122112))
	- There’s been some exciting work in this space, from @eleutherAI’s lm-eval to @langchainAI’s LLM-based eval.  
	  Every distinct prompt can necessitate a *new* evaluation metric. It'll become crucial for users to establish evaluation criteria to optimize prompts for their use case. ([View Tweet](https://twitter.com/jerryjliu0/status/1611402511801516032))
	- (3) Testing, monitoring, and failure protection will become just as important, if not more important, for LLM apps.
	- (4) All of the previous steps are necessary *even if* most companies don’t adopt finetuning. If they do, then they will need additional services (e.g. @scale_AI) that can help each company achieve the data ingestion, labeling, finetuning flywheel. 
	  https://t.co/43cjGdResG ([View Tweet](https://twitter.com/jerryjliu0/status/1611402514745917440))