title:: One Common Pain Point We... (highlights)
author:: [[@hwchase17 on Twitter]]
full-title:: "One Common Pain Point We..."
category:: #tweets
url:: https://twitter.com/hwchase17/status/1633527776803184652

- Highlights first synced by [[Readwise]] [[Mar 9th, 2023]]
	- One common pain point we heard is that ChatGPT does not work amazingly with preconfigured @LangChainAI chains
	  
	  This is because we have hardcoded default prompts that are optimized for GPT3
	  
	  Our (simple) solution? ✨Prompt Selectors✨
	  
	  https://t.co/FWJZPS5KAx
	  
	  🧵 ([View Tweet](https://twitter.com/hwchase17/status/1633527776803184652))
		- **Note**: Thread
	- Rather than have a default PromptTemplate, we will move towards having PromptSelectors
	  
	  These will take in the model passed in and based on the type of the model will select a PromptTemplate to use
	  
	  You are still able to pass in a custom PromptTemplate to use should you choose ([View Tweet](https://twitter.com/hwchase17/status/1633527779160637440))
	- The logic for selecting the PromptTemplate to use can be highly configurable
	  
	  To start, we're adding different PromptTemplates for "normal LLM" vs "chat model"
	  
	  The next step is different PromptTemplates for OpenAI vs Cohere, or even `text-davinci-002` vs `text-davinci-003` ([View Tweet](https://twitter.com/hwchase17/status/1633527780246966273))
	- It will take a while to completely move over from default PromptTemplates to PromptSelectors - and we could use a lot of help!
	  
	  In particular, if you have ChatGPT-specific prompt that works better than the default one, we'd love to get a PromptSelector set up with it! ([View Tweet](https://twitter.com/hwchase17/status/1633527781308121088))