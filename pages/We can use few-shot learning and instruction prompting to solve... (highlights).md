title:: We can use few-shot learning and instruction prompting to solve... (highlights)
author:: [[Cameron R. Wolfe]]
full-title:: "We can use few-shot learning and instruction prompting to solve..."
category:: #articles
url:: https://twitter.com/cwolferesearch/status/1655688722904432640
document_note:: We can use advanced prompting techniques to solve complex problems with existing large language models (LLMs). Three approaches discussed include Chain of Thought Prompting (CoT) to improve reasoning capabilities, Knowledge Augmentation to provide relevant information and prevent hallucinations, and Automatic Prompting to learn an optimal prompt from data. CoT prompting has already drastically improved LLM performance on commonsense, arithmetic, and symbolic reasoning benchmarks. However, techniques for automatic prompting cannot be used with paid APIs like OpenAI due to lack of access to the model's embedding layer. For more details on advanced prompt engineering topics, read the overview provided.
tags:: #[[LLMs]] #[[prompt engineering]]

- Highlights first synced by [[Readwise]] [[May 15th, 2023]]
	- Chain of Thought (CoT) Prompting
	  
	  LLMs are typically poor at solving multi-step or reasoning-based problems. CoT prompting mitigates this problem by encouraging LLMs via few-shot learning to generate a step-by-step problem-solving rationale along with their final answer. [2/8] ([View Highlight](https://read.readwise.io/read/01h07rrem27v99m1nnjkm18958))
		- **Note**: LLMs benefit from CoT prompting for reasoning-based problems.
	- Knowledge Augmentation
	  
	  Although LLMs learn a lot of information during pre-training, augmenting their prompts with relevant information is oftentimes helpful. In fact, this can help with notable problems like hallucination by providing the model with extra context. ([View Highlight](https://read.readwise.io/read/01h07rrq6c4h3n96etv4q4qbtn))
		- **Note**: Augmenting LLMs prompts with relevant info helps with hallucination.
	- Automatic Prompting
	  
	  Typically, prompt engineering involves tweaking the wording or structure of our prompt to see what works best. But, what if we could instead just learn an optimal prompt from data? This topic has been explored extensively in recent research. ([View Highlight](https://read.readwise.io/read/01h07rsw91f1fthef6fc0mb904))
		- **Note**: Automated prompt engineering using data.
	- ![](https://pbs.twimg.com/media/FvovbFgXsAAM8Tz.jpg) ([View Highlight](https://read.readwise.io/read/01h07rtbanb1s2mzvxe93tye6r))
		- **Tags**: #[[prompt engineering]]