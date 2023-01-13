title:: The 'Data Engine' Idea O... (highlights)
author:: [[@mathemagic1an on Twitter]]
full-title:: "The 'Data Engine' Idea O..."
category:: #tweets
url:: https://twitter.com/mathemagic1an/status/1607384423942742019

- Highlights first synced by [[Readwise]] [[Dec 27th, 2022]]
	- The 'data engine' idea of defensibility in AI may not be as defensible as we thought:
	  
	  In SELF-INSTRUCT, authors get [[GPT-3]] to generate it's *own* dataset for instruction tuning, outperforming vanilla GPT-3 and comparable to InstructGPT.
	  
	  https://t.co/xlsA5pCwnS
	  
	  Here's how 👇 
	  
	  ![](https://pbs.twimg.com/media/Fk6PvvjXoAApiv0.jpg) ([View Tweet](https://twitter.com/mathemagic1an/status/1607384423942742019))
		- **Note**: Thread
	- Within the LLM x startup world, the idea of a "data engine" is often discussed as a means of building a moat.
	  
	  The idea is to gather data as your model interacts with the real world => leverage these experiences to improve the model for your specific task 
	  
	  ![](https://pbs.twimg.com/media/Fk6QP_BXgAARE9S.jpg) ([View Tweet](https://twitter.com/mathemagic1an/status/1607384451205550083))
	- The defensibility comes from the idea that the models that amass more experience (i.e. are deployed earlier/broader) will improve faster over time, compounding returns.
	  
	  This assumes that deployment in the wild is the best way to gather the "fuel" for your data engine, however. ([View Tweet](https://twitter.com/mathemagic1an/status/1607384453373988866))
	- In SELF-INSTRUCT (2022), the authors have [[GPT-3]] generate a set of 82k samples for "instruction tuning" (essentially what OpenAI has claimed makes their models better/more aligned)
	  
	  This is basically sets of (task definition, pos/neg example, input/output instances) 
	  
	  ![](https://pbs.twimg.com/media/Fk6RcdNWAAAH0-b.png) ([View Tweet](https://twitter.com/mathemagic1an/status/1607384455005769728))
	- They find that [[GPT-3]] is able to generate a diverse set of new tasks to instruction tune itself with: 
	  
	  ![](https://pbs.twimg.com/media/Fk6RqXiWQAIGaM7.jpg) ([View Tweet](https://twitter.com/mathemagic1an/status/1607384457245298688))
	- And critically, they show that actually running instruction tuning with these [[GPT-3]]-generated samples performs as well as InstructGPT
	  
	  That is, using *synthetic* data for instruction tuning can perform as well as a traditional "data engine"! 
	  
	  ![](https://pbs.twimg.com/media/Fk6R7DUXkAMwb2_.jpg) ([View Tweet](https://twitter.com/mathemagic1an/status/1607384459342389249))
	- Their process is relatively simple and essentially involves an iterative cycle of generating and filtering samples for instruction tuning.
	  
	  Seems straightforward to reproduce even on a closed model like OpenAIs' GPT ecosystem (as the authors did here) 
	  
	  ![](https://pbs.twimg.com/media/Fk6S2CpXoAAow9Z.png) 
	  
	  ![](https://pbs.twimg.com/media/Fk6TAjrXkAAuTv8.png) ([View Tweet](https://twitter.com/mathemagic1an/status/1607384461510852608))
	- This is very promising as an approach for startups and resource-poor outfits trying to achieve high performance IMO
	  
	  Barrier to entry is low: literally see if you can generate synthetic tasks/samples in your domain for instruction tuning, then fine-tune + evaluate. ([View Tweet](https://twitter.com/mathemagic1an/status/1607384633636974594))