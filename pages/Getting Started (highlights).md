title:: Getting Started (highlights)
author:: [[langchain.readthedocs.io]]
full-title:: "Getting Started"
category:: #articles
url:: https://langchain.readthedocs.io/en/latest/modules/prompts/getting_started.html
tags:: #[[langchain]]

- Highlights first synced by [[Readwise]] [[Mar 12th, 2023]]
	- A prompt template refers to a reproducible way to generate a prompt. It contains a text string (“the template”), that can take in a set of parameters from the end user and generate a prompt.
	  
	  The prompt template may contain: ([View Highlight](https://read.readwise.io/read/01gva1v86jys5br0b23jbtj2zb))
	- Few shot examples are a set of examples that can be used to help the language model generate a better response.
	  
	  To generate a prompt with few shot examples, you can use the `FewShotPromptTemplate`. This class takes in a `PromptTemplate` and a list of few shot examples. It then formats the prompt template with the few shot examples. ([View Highlight](https://read.readwise.io/read/01gva1v25ex9t9dqp0rgkxw29p))