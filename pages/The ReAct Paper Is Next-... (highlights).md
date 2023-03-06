title:: The ReAct Paper Is Next-... (highlights)
author:: [[@RazRazcle on Twitter]]
full-title:: "The ReAct Paper Is Next-..."
category:: #tweets
url:: https://twitter.com/RazRazcle/status/1622033232232611841

- Highlights first synced by [[Readwise]] [[Feb 5th, 2023]]
	- The ReAct Paper is next-level prompt engineering.
	  
	  If you understand how it works then you can start building LLM apps that are way more factual than chatGPT and can use external APIs and tools. Check-out the example at the end.
	  
	  To understand ReAct, let's think step-by-step: 
	  
	  ![](https://pbs.twimg.com/media/FoKen95aQAAcYTk.png) ([View Tweet](https://twitter.com/RazRazcle/status/1622033232232611841))
		- **Note**: Thread
	- 1/ The simplest possible prompt is a "zero-shot" instruction prompt. You just ask the model to do what you want. This works *ok* but the model still has a tendency to make things up and it doesn't know about changing world events or private info. 
	  
	  ![](https://pbs.twimg.com/media/FoKeooOaQAkU80v.jpg) ([View Tweet](https://twitter.com/RazRazcle/status/1622033244215726080))
	- 2/You can improve factual accuracy by including external knowledge or APIs in the prompt.
	  You can even let the model specify what extra info it needs through a very simple "domain specific language" . If the model outputs "google: a query", you append the results of that query. 
	  
	  ![](https://pbs.twimg.com/media/FoKepPTagAEuuGV.png) ([View Tweet](https://twitter.com/RazRazcle/status/1622033253585809408))
	- 3/ Action-prompting is ok for simple questions but if the question requires reasoning then it tends to fail.
	  
	   "Chain of Thought" prompting lets you over come this. In your prompt you include explicit reasoning and this gets the model to do the same. This increases accuracy: 
	  
	  ![](https://pbs.twimg.com/media/FoKepybaMAAInhC.png) ([View Tweet](https://twitter.com/RazRazcle/status/1622033263727632385))
	- 4/ The simple but powerful idea in ReAct is to combing action-prompts with chain-of-thought. Taken together this helps the model to reason about what actions to take. It's much more powerful: 
	  
	  ![](https://pbs.twimg.com/media/FoKeqYjaEAAxJbr.png) ([View Tweet](https://twitter.com/RazRazcle/status/1622033275148722176))
	- 5/ Here's a concrete example of a ReAct style prompt I used to build an automatic sales email generator.
	  
	  You need to execute the "search" actions from the LLM and append the results from google. @humanloop tools makes this super easy. 
	  
	  ![](https://pbs.twimg.com/media/FoKerDGaEAABoMt.jpg) ([View Tweet](https://twitter.com/RazRazcle/status/1622033284975972352))
- New highlights added [[Feb 25th, 2023]] at 5:56 PM
	- @dylan_alloy Is* ([View Tweet](https://twitter.com/RazRazcle/status/1622218682138075139))