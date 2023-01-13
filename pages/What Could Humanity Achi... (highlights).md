title:: What Could Humanity Achi... (highlights)
author:: [[@mathemagic1an on Twitter]]
full-title:: "What Could Humanity Achi..."
category:: #tweets
url:: https://twitter.com/mathemagic1an/status/1607767768400543745

- Highlights first synced by [[Readwise]] [[Dec 28th, 2022]]
	- What could humanity achieve with an AI that can reason generally about videos?
	  
	  In InternVideo, the authors debut a powerful foundation model for video, achieving SOTA results on dozens of video/language tasks
	  
	  https://t.co/uOcadM1WTt
	  
	  Some highlights 👇 
	  
	  ![](https://pbs.twimg.com/media/Fk_s1-QWYAEIj5u.jpg) ([View Tweet](https://twitter.com/mathemagic1an/status/1607767768400543745))
		- **Note**: Thread
	- "Foundation models," a term coined (and aggressively pushed) by Stanford, are models that are trained once and can be adapted to solve a broad set of downstream tasks.
	  
	  [[GPT-3]], for instance, a language foundation model, can:
	- This is a significant departure from old-school (pre-2020s) ML:
	  
	  You used to have to train a single model per task. This is time-intensive and means you need ML expertise if you have an ML-related application in mind.
	  
	  No longer the case! ([View Tweet](https://twitter.com/mathemagic1an/status/1607767773803081736))
	- With InternVideo, a team from across China brings foundation models to video (a first)
	  
	  This model shows significant improvement in the SOTA for a variety of diverse tasks. Truly impressive. 
	  
	  ![](https://pbs.twimg.com/media/Fk_uColXwAIAtMV.jpg) ([View Tweet](https://twitter.com/mathemagic1an/status/1607767775757352960))
	- They train it with two separate training regimes:
	  
	  Masked video modeling: basically predict what happens next in a video
	  
	  Video-language contrastive learning: basically look at an aligned (video, description) pair separately, and learn to form similar representations of the two 
	  
	  ![](https://pbs.twimg.com/media/Fk_ucaJWIAQyW8k.jpg) ([View Tweet](https://twitter.com/mathemagic1an/status/1607767778395668481))
	- They present several other clever innovations in the paper, including how they perform inference and other learning hacks. For more info check out the article, 
	  
	  ![](https://pbs.twimg.com/media/Fk_u_TSWYAE0Fd6.jpg) ([View Tweet](https://twitter.com/mathemagic1an/status/1607767780471836675))
	- But the TL;DR here is that we now have a single model that does all of the above (in video):
	- ...
	- The takeaway:
	  
	  If you are tackling a problem involving the interpretation of video, you may be able to soon scrap your ML stack and instead rely on an OpenAI-like API that will adapt to your task.
	  
	  So many new ideas now seem doable within a startup context. ([View Tweet](https://twitter.com/mathemagic1an/status/1607767785832079360))
	- Also just want to call attention to their impressive and gratuitous amount of tags on their Github for SOTA status.
	  
	  (Kudos for making the code OSS)
	  
	  https://t.co/wN1PVaDlCl 
	  
	  ![](https://pbs.twimg.com/media/FlAEOOhWQAANUHa.jpg) ([View Tweet](https://twitter.com/mathemagic1an/status/1607789752572600320))