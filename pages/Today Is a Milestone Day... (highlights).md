title:: Today Is a Milestone Day... (highlights)
author:: [[@NateSooter on Twitter]]
full-title:: "Today Is a Milestone Day..."
category:: #tweets
url:: https://twitter.com/NateSooter/status/1472968046910132225

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Today is a milestone day. 10 months ago, data leadership took a chance on "analytics engineering" after I kept insisting on it.  They said "OK - you lead a team of 2 others, go build." 
	  
	  Today our core database launches (& more!). It's been quite a journey, time for a🧵 ([View Tweet](https://twitter.com/NateSooter/status/1472968046910132225))
		- **Note**: Thread
	- Three major problems existed before we formed:
	  
	  (1) Multiple legacy databases with 1,000+ tables. All undocumented.
	  
	  (2) Analysts could only ship code every 1-2 weeks. The reasons for this internally were sound but very bad for analysts. But it was the only option available. ([View Tweet](https://twitter.com/NateSooter/status/1472968048105508864))
	- (3) Analysts got around #2 by shipping code via Tableau. Since Tableau could hold custom SQL and could run on a schedule, it became the defacto analytics production pipeline. Thousands and thousands of Tableau reports appeared as a result. ([View Tweet](https://twitter.com/NateSooter/status/1472968049212809226))
	- -- a light appears --
	  
	  A few analysts get frustrated about this (@sethrosen was right -- https://t.co/HEiElx8sUJ).
	  
	  We realize we're all building parallel data pipelines in silos. Wasting time & energy & work. ([View Tweet](https://twitter.com/NateSooter/status/1472968050391478278))
	- Around 2 years ago, one teammate in particular builds out a "Base" schema with core tables needed for some teams. I add into it, over time many people start leveraging it. ([View Tweet](https://twitter.com/NateSooter/status/1472968051691687936))
	- While this is happening, I learn about the @LocalOptimistic community and put a name to what we're working on - Analytics Engineering. Just having a term for it was immensely helpful. I come from a sales background, so I start selling - we need to make an AE team. ([View Tweet](https://twitter.com/NateSooter/status/1472968052899672065))
	- My manager is supportive of the plan, even though it means myself & one other would leave his team. 
	  
	  I put together slide decks and meetings and eventually our SVP agrees - it's time to form the AE team. 
	  
	  On Valentines Day 2021, our team is official. A true data love story. ([View Tweet](https://twitter.com/NateSooter/status/1472968054027870209))
	- Here's the interesting twist: we didn't realize what we were signing up for. Seems like it always turns out that way.
	  
	  We THOUGHT we were solving problem #1 (hard to find data) by just...making more tables in the pre-existing Base schema. Easy, right?
	  
	  Except... ([View Tweet](https://twitter.com/NateSooter/status/1472968055139418112))
	- A month or two in we realize we can change...everything. 
	  
	  What if we had our own database?
	  What if we owned our own transformation pipeline?
	  What if we made it so analysts could ship early and often, instead of bi-weekly? 
	  What if we had our own set of tools (@getdbt, git repo)? ([View Tweet](https://twitter.com/NateSooter/status/1472968056154451976))
	- Suddenly, our project wasn't "make some more tables in that one schema everyone likes". It was threefold:
	  
	  (1) Design a database that works across all departments. one schema won't do that.
	  
	  (2) Take control of tools & processes
	  
	  (3) Revamp how analytics code is committed for all ([View Tweet](https://twitter.com/NateSooter/status/1472968057232379910))
	- That moved our project from "We'll ship some stuff in a few months" to "wow, we have a lot to do, maybe by the end of the year we'll have something ready."  And an unbelievable marathon sprint toward V1 began. ([View Tweet](https://twitter.com/NateSooter/status/1472968058310250496))
	- We had to learn dbt from the ground up. We had to create & manage our own databases. We had to learn how control our own git repo. We needed to spin up VMs to run everything. We had to connect all of that together.
	  
	  All while building the core tables the company needed. ([View Tweet](https://twitter.com/NateSooter/status/1472968059426009088))
	- Today we launch with all the above and solutions to the three problems outlined above:
	  
	  (a) 71 documented, productionalized tables
	  (b) A method for analysts to contribute code early & often
	  (c) ~50% of all workbooks have been deprecated in 3 months ([View Tweet](https://twitter.com/NateSooter/status/1472968060554203140))
	- This is just the start of everything. Now the hard work of breaking habits begins - moving data from silos built by individual analysts into code contributed to our repo. Depend less on Tableau, more on dbt. Sell to other teams why they should use our database. ([View Tweet](https://twitter.com/NateSooter/status/1472968061573472264))
	- But before that hard work begins, it's time to take a breath.  Look back, appreciate where we started & where we've arrived.  The hours have been long. The stress high. 
	  
	  But we can be proud of what we did in 10 short months. We've built a foundation that will last. ([View Tweet](https://twitter.com/NateSooter/status/1472968062772989952))
		- **Tags**: #[[favorite]]
	- My team isn't on Twitter so I can't mention them directly, but I'm really amazed by the work the two of them did. Really brilliant work.  Couldn't be more proud to launch this project alongside them. Can't wait to see what else we create together. ([View Tweet](https://twitter.com/NateSooter/status/1472968063821574147))
	- To end the thread - I want to say thanks. Thanks to leadership rolling the dice with me. Thanks to my team. Thanks to @matsonj for daily discussions & advice.  Thanks to the @LocalOptimistic and @getdbt Slack communities for their ideas & discussions. ([View Tweet](https://twitter.com/NateSooter/status/1472968064836661250))
	- And thank you Data Twitter. We don't launch today without the wisdom shared here.  I'm not the most active participant, but I am a daily reader. And without all of you, our AE team doesn't even exist and this project never comes to fruition.
	  
	  Today, I'm thankful.
	  
	  /🧵 ([View Tweet](https://twitter.com/NateSooter/status/1472968065977503747))