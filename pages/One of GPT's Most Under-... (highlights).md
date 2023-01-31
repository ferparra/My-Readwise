title:: One of GPT's Most Under-... (highlights)
author:: [[@petepetrash on Twitter]]
full-title:: "One of GPT's Most Under-..."
category:: #tweets
url:: https://twitter.com/petepetrash/status/1619578203143798791

- Highlights first synced by [[Readwise]] [[Jan 30th, 2023]]
	- One of GPT's most under-appreciated features is one-shot structuring of unstructured data. The possibilities of this are far reaching and can unlock massive productivity boosts in many domains. This will be a thread of some experiments applying this to clinical note-taking 👇 ([View Tweet](https://twitter.com/petepetrash/status/1619578203143798791))
		- **Note**: Thread
	- With not a lot of experience using the GPT API and some rudimentary prompt engineering, I can turn the following clinical note into this JSON, which follows a schema I specified: 
	  
	  ![](https://pbs.twimg.com/media/Fnnobx_aIAE2cvE.png) 
	  
	  ![](https://pbs.twimg.com/media/FnnoiaYaYAIfdRX.jpg) ([View Tweet](https://twitter.com/petepetrash/status/1619581224498114560))
	- Like most tools and even companies building on top of the GPT API, a clever prompt can provide a stunning amount of leverage. The prompt I prepended to the clinical note input does a few key things: ([View Tweet](https://twitter.com/petepetrash/status/1619581898124328960))
	- 1. If your structured data includes any date fields, you'll need to tell GPT what the current date is. Otherwise it assumes it's 2020 by default. 
	  
	  This is as simple as `Today's date is ${new Date()}` at the start of the prompt. ([View Tweet](https://twitter.com/petepetrash/status/1619582972340076544))
	- 2a. Context priming: This is incredibly weird and awesome. You're essentially telling GPT a story about itself—its origin and it's purpose in life. Cont. ([View Tweet](https://twitter.com/petepetrash/status/1619584120639848448))
	- 2b. This is how I bootstrapped GPT to orient itself towards my input: 
	  
	  "You're a sophisticated NLP model trained on the mental health domain as well as clinical shorthand, abbreviations, and terminology." ([View Tweet](https://twitter.com/petepetrash/status/1619584410323664896))
	- 3a. Get very specific about how you want the data to be structured. I know I want JSON, and my application data follows a particular schema. I also need to need to be mindful of the 4k token budget which counts against the prompt + output. Cont.. ([View Tweet](https://twitter.com/petepetrash/status/1619585105667948546))
	- 3b. Providing a full JSON object with example values gets the job done, though it turns out if you're using a typed language (I'm using TypeScript), you can just provide the type interface! This approach enables some other capabilities, like narrowing using unions: 
	  
	  ![](https://pbs.twimg.com/media/FnnuSwDagAAC9EV.png) ([View Tweet](https://twitter.com/petepetrash/status/1619587556261396480))
	- 3c. These types not comprehensive; just for testing. You may have noticed that I added comments to some fields. This is something I'm in the middle of experimenting with to further steer the output in the desired direction on a per-field basis. Seems to be working fairly well. ([View Tweet](https://twitter.com/petepetrash/status/1619588300247007234))
	- 4. Glue it all together. Here is the complete prompt I used to structure that example clinical note. All line breaks are removed, and there are additional instructions I'm experimenting with to further refine the output: 
	  
	  ![](https://pbs.twimg.com/media/FnnwAKTaEAEYhUW.png) ([View Tweet](https://twitter.com/petepetrash/status/1619589435062095873))
	- The preamble is currently 374 tokens. The continuation response is ~790. This would allow around 2,800 tokens in the clinical note (the mock note I used is 390) which is ~2,100 words. I'm certain the preamble and response can be brought down a lot, so there is plenty of headroom. ([View Tweet](https://twitter.com/petepetrash/status/1619591255721410563))
	- Next up is the UI side of the equation which I'm excited to explore and share more about.
	  
	  If you're doing similar work or have any feedback, advice, or questions, hit me up :) ([View Tweet](https://twitter.com/petepetrash/status/1619592118036725765))
	- Here's a breakdown of the structured output based on the clinical note example. Aside from faithfully adhering to the provided schema, GPT was able to make some impressive inferences: 
	  
	  ![](https://pbs.twimg.com/media/FnqtpTiaAAIhKWh.jpg) ([View Tweet](https://twitter.com/petepetrash/status/1619798625353347072))