title:: LangChain Just Announced... (highlights)
author:: [[@ankush_gola11 on Twitter]]
full-title:: "LangChain Just Announced..."
category:: #tweets
url:: https://twitter.com/ankush_gola11/status/1630973639184232450

- Highlights first synced by [[Readwise]] [[Mar 6th, 2023]]
	- LangChain just announced a new Toolkit abstraction that allows developers to create agents designed for a particular use-case. We leveraged toolkits to build an agent capable of looking through an OpenAPI spec and making a correct API request based on the spec. Let's unpack this: 
	  
	  ![](https://pbs.twimg.com/media/FqJh04eaAAUCVZC.jpg) ([View Tweet](https://twitter.com/ankush_gola11/status/1630973639184232450))
		- **Note**: Thread
	- The agent is asked to make a request to the OpenAI completions endpoint, with the prompt being "tell me a joke" (very meta, I know). The agent is equipped with a toolkit for making various HTTP requests and inspecting a large JSON blob (in this case, the OpenAI API spec). ([View Tweet](https://twitter.com/ankush_gola11/status/1630973771447427072))
	- It's important to note that the entire OpenAI API spec is too large to fit in the context window of an LLM. With the proper tool, the agent is able to retrieve small parts of the spec bit by bit and decide where in the spec to inspect next. ([View Tweet](https://twitter.com/ankush_gola11/status/1630973846479323136))
	- First, the agent looks for the correct base url. Those familiar with LangChain should pick on the fact that this agent is using another agent as a tool (see JSON agent https://t.co/lFpOdAFhtD). 
	  
	  ![](https://pbs.twimg.com/media/FqJiL-2aIAEL-Nb.jpg) ([View Tweet](https://twitter.com/ankush_gola11/status/1630973980785131520))
	- Next, the agent looks through the spec to find the correct path and required request body parameters. 
	  
	  ![](https://pbs.twimg.com/media/FqJiSy9aIAA9ctd.jpg) ([View Tweet](https://twitter.com/ankush_gola11/status/1630974101937598466))
	- Finally, the agent uses another tool to make the POST request to the completions endpoint with the required model parameter. 
	  
	  ![](https://pbs.twimg.com/media/FqJiZp-acAAr9r4.jpg) ([View Tweet](https://twitter.com/ankush_gola11/status/1630974229947768834))
	- I'll admit that this is example is a bit contrived -- there's no need to use an agent with an API spec to make a request to OpenAI. An LLM can probably give you the curl command or write you some python code to that already, out-of-the-box. ([View Tweet](https://twitter.com/ankush_gola11/status/1630974307844390912))
	- However, the principles in this example definitely demonstrate the power of LangChain's Toolkit abstraction. ([View Tweet](https://twitter.com/ankush_gola11/status/1630974618885586944))
	- By allowing developers to create specialized agents, we can automate complex tasks that would otherwise require significant manual effort, such as sifting through a complex API spec to figure out how to make a request. ([View Tweet](https://twitter.com/ankush_gola11/status/1630974762217537541))
	- The ability to analyze and take actions based on large amounts of data in a structured way is a valuable skill for agents, and LangChain's Toolkits make it easier than ever to do so.
	  
	  Let us know if there are other examples you want to see! ([View Tweet](https://twitter.com/ankush_gola11/status/1630975030652981248))
	- Full tweet here with more examples: https://t.co/ofge6a5wDZ
	  
	  And blogpost here: https://t.co/OlO6LcnI3p ([View Tweet](https://twitter.com/ankush_gola11/status/1630975285062672385))