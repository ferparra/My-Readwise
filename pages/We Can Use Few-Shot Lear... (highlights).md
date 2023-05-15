title:: We Can Use Few-Shot Lear... (highlights)
author:: [[@cwolferesearch on Twitter]]
full-title:: "We Can Use Few-Shot Lear..."
category:: #tweets
url:: https://twitter.com/cwolferesearch/status/1655688722904432640

- Highlights first synced by [[Readwise]] [[May 15th, 2023]]
	- We can use few-shot learning and instruction prompting to solve many problems with large language models (LLMs), but what should we do when these techniques fall short? Here are three advanced prompting approaches that can be used to solve complex problems with LLMs… 🧵 [1/8] 
	  
	  ![](https://pbs.twimg.com/media/Fvou3b3XgAAD0wg.jpg) ([View Tweet](https://twitter.com/cwolferesearch/status/1655688722904432640))
		- **Note**: Thread
	- 1. Chain of Thought (CoT) Prompting
	  
	  LLMs are typically poor at solving multi-step or reasoning-based problems. CoT prompting mitigates this problem by encouraging LLMs via few-shot learning to generate a step-by-step problem-solving rationale along with their final answer. [2/8] 
	  
	  ![](https://pbs.twimg.com/media/Fvou89jX0AImyqV.jpg) ([View Tweet](https://twitter.com/cwolferesearch/status/1655688724082982916))
	- Prior work has shown that teaching language models (e.g., via fine-tuning) to generate problem-solving rationales improves their reasoning capabilities. CoT prompting drastically improves LLM performance on commonsense, arithmetic, and symbolic reasoning benchmarks. [3/8] 
	  
	  ![](https://pbs.twimg.com/media/FvovAgeWwAAoMr8.jpg) ([View Tweet](https://twitter.com/cwolferesearch/status/1655688725219749888))
	- 2. Knowledge Augmentation
	  
	  Although LLMs learn a lot of information during pre-training, augmenting their prompts with relevant information is oftentimes helpful. In fact, this can help with notable problems like hallucination by providing the model with extra context. [4/8] 
	  
	  ![](https://pbs.twimg.com/media/FvovI4SWcAAjqFz.jpg) ([View Tweet](https://twitter.com/cwolferesearch/status/1655688726394159110))
	- Several knowledge augmentation approaches exist. For example, we can store/retrieve textual information from a vector database. Alternatively, we could follow a generated knowledge approach that prompts a separate LLM to generate additional context to be included. [5/8] 
	  
	  ![](https://pbs.twimg.com/media/FvovSoYWAAMt7l0.jpg) ([View Tweet](https://twitter.com/cwolferesearch/status/1655688727589535750))
	- 3. Automatic Prompting
	  
	  Typically, prompt engineering involves tweaking the wording or structure of our prompt to see what works best. But, what if we could instead just learn an optimal prompt from data? This topic has been explored extensively in recent research. [6/8] 
	  
	  ![](https://pbs.twimg.com/media/FvovbFgXsAAM8Tz.jpg) ([View Tweet](https://twitter.com/cwolferesearch/status/1655688728893874177))
	- For more details on approaches for automatic prompting, check out the tweet below. Unfortunately, such techniques cannot be used with paid APIs (e.g., from OpenAI) due to the lack of access to the model’s embedding layer. [7/8]
	  
	  https://t.co/6RCvha3Ivu ([View Tweet](https://twitter.com/cwolferesearch/status/1655688730097623041))
	- TL;DR: several advanced prompting techniques exist that can be used to solve surprisingly complex problems with existing LLMs. For more details, check out my overview of advanced topics in prompt engineering below.
	  
	  🔗: https://t.co/GEc9nno1jY
	  
	  [8/8] ([View Tweet](https://twitter.com/cwolferesearch/status/1655688731402051584))