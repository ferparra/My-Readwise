title:: BabyAGI X @LangChainAI!... (highlights)
author:: [[@pictobit on Twitter]]
full-title:: "BabyAGI X @LangChainAI!..."
category:: #tweets
url:: https://twitter.com/pictobit/status/1645477658958888973

- Highlights first synced by [[Readwise]] [[Apr 13th, 2023]]
	- BabyAGI x @LangChainAI!
	  Yet another take on the BabyAGI concept. This one has a couple architectural changes, more focused on solving complex pronlems rather than AGI, and can be integrated with other langchain projects (thanks for the demo notebook!) @hwchase17 ([View Tweet](https://twitter.com/pictobit/status/1645477658958888973))
		- **Note**: Thread
	- Here's how it works!
	  First, the code: https://t.co/RitmuvMHoU ([View Tweet](https://twitter.com/pictobit/status/1645477661601300487))
	- This is a system with 4 actors: planner, executor, learner and reviewer. They all form a loop that breaks down a complex problem into a series of steps, and executes it ([View Tweet](https://twitter.com/pictobit/status/1645477665426505759))
	- The planner runs once at the start, it thinks of a strategy to solve the problem, and produces a task list ([View Tweet](https://twitter.com/pictobit/status/1645477668349935626))
	- The executor is a custom langchain agent, which implements ReAct to solve a single task in the plan. It can be provided any tools in the langchain format ([View Tweet](https://twitter.com/pictobit/status/1645477671692795912))
	- Here's the interesting part. The system holds an information context string, which starts empty. After each step, the learner merges the result with the current context, as a sort of medium-term memory ([View Tweet](https://twitter.com/pictobit/status/1645477674448453666))
	- The reviewer assesses the current task list, based on the current completed tasks and generated info context, and reprioritizes the pending tasks accordingly ([View Tweet](https://twitter.com/pictobit/status/1645477677493518366))
	- As I mentioned, the system built to eventually terminate. It tries to reach the final goal in a concise number of steps ([View Tweet](https://twitter.com/pictobit/status/1645477680001712149))
	- Right now, the main limitation is the limited info context. As a next step, I'm planning on adding a "long term memory agent", that extracts information from the context, replacing it with a key. The executor agent will then be provided a tool to retrieve these saved snippets ([View Tweet](https://twitter.com/pictobit/status/1645477682631548928))
	- Forgot to thank @yoheinakajima for starting all this of course! ([View Tweet](https://twitter.com/pictobit/status/1645481273148817408))
	- A simple demo https://t.co/A2WFzPqZ9f ([View Tweet](https://twitter.com/pictobit/status/1645504308874563584))
	- I wonder what this becomes in a few months with GPT-4 32k ([View Tweet](https://twitter.com/pictobit/status/1645518023900495891))