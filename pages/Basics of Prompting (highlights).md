title:: Basics of Prompting (highlights)
author:: [[promptingguide.ai]]
full-title:: "Basics of Prompting"
category:: #articles
url:: https://www.promptingguide.ai/introduction/basics

- Highlights first synced by [[Readwise]] [[Apr 13th, 2023]]
	- This can be formatted into a question answering (QA) format, which is standard in a lot of QA datasets, as follows:
	  
	    Q: <Question>?
	    A: 
	  
	  When prompting like the above, it's also referred to as *zero-shot prompting*, i.e., you are directly prompting the model for a response without any examples or demonstrations about the task you want it to achieve. Some large language models do have the ability to perform zero-shot prompting but it depends on the complexity and knowledge of the task at hand. ([View Highlight](https://read.readwise.io/read/01gxhj9bx5enrzpe2mw68ptnm8))
	- Given the standard format above, one popular and effective technique to prompting is referred to as *few-shot prompting* where we provide exemplars (i.e., demonstrations). Few-shot prompts can be formatted as follows:
	  
	    <Question>?
	    <Answer>
	    
	    <Question>?
	    <Answer>
	    
	    <Question>?
	    <Answer>
	    
	    <Question>? ([View Highlight](https://read.readwise.io/read/01gxhj9sm4gn70fme7nfw8qcb3))