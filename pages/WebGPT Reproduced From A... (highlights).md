title:: WebGPT Reproduced From A... (highlights)
author:: [[@dust4ai on Twitter]]
full-title:: "WebGPT Reproduced From A..."
category:: #tweets
url:: https://twitter.com/dust4ai/status/1587104029712203778

- Highlights first synced by [[Readwise]] [[Feb 25th, 2023]]
	- WebGPT reproduced from advanced prompting only.
	  
	  Dust-based web-search assistant demo answers questions by searching the web, summarizing content and compiling a final answer with references:
	  
	  https://t.co/099gsuJ4Xx 
	  
	  ![](https://pbs.twimg.com/media/FgaDWOJWYAAVmL-.jpg) ([View Tweet](https://twitter.com/dust4ai/status/1587104029712203778))
		- **Note**: Thread
	- This app performs the following steps:
	  
	  1/ search google, take first 3 results
	  2/ call to a @Replit to get content (headless browsing)
	  3/ 1st model call to clean-up and summarize each site
	  4/ 2nd model call (few-shot prompted) to generate final answer with references ([View Tweet](https://twitter.com/dust4ai/status/1587104033696784385))
	- Step 1/ 2/ 3/ replace browsing / clicking / scrolling / selecting with a more direct API-based approach. Less shiny but more resilient. ([View Tweet](https://twitter.com/dust4ai/status/1587104035601108993))
	- Note that text-davinci-002 is really good at step 3/ out of the box without few-shot examples. Hypothesis: Instruct-series training set probably includes a lot of summarization tasks. ([View Tweet](https://twitter.com/dust4ai/status/1587104037815681024))
	- Step 4/ required few-shot prompting to teach the model how to aggregate content and generate references. Two examples were sufficient! Completely fails otherwise. 
	  
	  ![](https://pbs.twimg.com/media/FgaGOksXgAA_8Fk.png) ([View Tweet](https://twitter.com/dust4ai/status/1587104045961039873))
	- Original WebGPT used 6000 human demonstrations. This uses tools (@replit packaged headless browsing) + APIs (google) + 2 examples.
	  
	  We hypothesize that data and symbolic structure can be traded for many use-cases. We'll eval this app against the same benchmarks to confirm this. 
	  
	  ![](https://pbs.twimg.com/media/FgaFtTNXkAUsm54.png) ([View Tweet](https://twitter.com/dust4ai/status/1587104053691031554))
	- Study the app here: https://t.co/099gsuJ4Xx
	  
	  Looking forward to see how this can be adapted to productive use-cases without the need for collecting human trajectories. ([View Tweet](https://twitter.com/dust4ai/status/1587104056211800071))