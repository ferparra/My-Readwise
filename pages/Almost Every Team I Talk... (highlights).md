title:: Almost Every Team I Talk... (highlights)
author:: [[@bbalfour on Twitter]]
full-title:: "Almost Every Team I Talk..."
category:: #tweets
url:: https://twitter.com/bbalfour/status/1311779272843952128

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- Almost every team I talk to says "Our data is mess!" 
	  
	  @crystalwidjaja (Fmr SVP BI & Growth at Gojek and @Reforge Partner) wrote an excellent piece on the real root causes of analytics failures, and a step by step process on how she thinks about it: https://t.co/UAr7KQTXR7
	  
	  🧵👇
		- **Tags**: #[[favorite]]
	- First, if you don't know @crystalwidjaja and the story of Gojek, it's impressive.  Crystal joined at 30 people and helped them scale to complete more daily food orders than Grubhub, Uber Eats, and DoorDash combined, and more trips than Lyft per day 🤯
	- There are a lot of symptoms of bad analytics/data:
	  
	  1. Lack of shared language
	  2. Slow transfer of knowledge
	  3. Lack of trust
	  4. Inability to act on data quickly
	  
	  ...
		- **Tags**: #[[favorite]]
	- ...but these are the symptoms.  The real root causes of these symptoms tend to come down to one or more things:
	  
	  1. Tracking metrics vs analyzing metrics as the goal. Those two things are very different, with the latter being making information actionable.  
	  
	  ...
		- **Tags**: #[[favorite]]
	- 2. Having a developer/data mindset vs business user mindset.  A core principle of building any good product is deeply understanding your target user.  When building data systems many teams lose sight of who their customer is, or don't have one in mind at all - the business user.
	- 3. Wrong level of abstraction.  Bad tracking is when our events are too broad, good tracking is when our events are too specific, great tracking is when we have balanced the two. (example in the full post)
	- 4. Written Only vs Visual communication. No matter how well we name or define events and properties, nothing is more clear than a visual that corresponds with an event.
	- 5. The good old data wheel of death. https://t.co/7jmkxhOrFr
	- So what to do instead? Crystal provided a step by step on how she thinks through the instrumentation process.  
	  
	  Full process is in the post(https://t.co/UAr7KQTXR7) 
	  
	  But some of my favorite points...
	- A. To get to the right level of abstraction, you need to track journey's of intent, success, and failure NOT metrics.
	- B. One of the most commonly missed, but important properties on events are contextual properties to help understand what might influence user motivation. For example, how many drivers on the screen when booking in a ride-sharing app?
		- **Tags**: #[[growth]] #[[favorite]]
	- C. Pressure test your analytics plan with three audiences.  Business users close to product development, biz users farther away from product dev (i.e. customer support) and new employees.  All have different levels of knowledge/perspective.
	- D. Keep a "decisions made without data" sheet every quarter to help uncover things you overlooked or didn't anticipate.
		- **Tags**: #[[favorite]]