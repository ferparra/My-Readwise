title:: If You Didn't Make It To... (highlights)
author:: [[@teej_m on Twitter]]
full-title:: "If You Didn't Make It To..."
category:: #tweets
url:: https://twitter.com/teej_m/status/1567622047739805696

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- If you didn't make it to Snowflake Summit, you missed my talk on funnels!
	  
	  "Funnel analysis" is an old marketing term adopted by web & app analytics to measure cohort behavior, onboarding dropoff, and navigation paths.
	  
	  Measuring funnels in SQL is slow and painful. Let's fix that 
	  
	  ![](https://pbs.twimg.com/media/FcFDzIAaUAA25hU.jpg) ([View Tweet](https://twitter.com/teej_m/status/1567622047739805696))
		- **Note**: Thread
	- I define a funnel as any process comprised of:
	- In the web world we call this a funnel, but this definition applies to many different types of analysis. 
	  
	  ![](https://pbs.twimg.com/media/FcFEYdSaMAAgeO4.jpg) ([View Tweet](https://twitter.com/teej_m/status/1567622145890725888))
	- There are common approaches to funnel analysis in SQL: the join, windows, or regex.
	  
	  A LEFT JOIN is the foundational approach and the easiest to write, despite not being fast. You should start here.
	  
	  In my examples, I use a single events table, and self-join it to model my funnel 
	  
	  ![](https://pbs.twimg.com/media/FcFFCx1aMAAuNP6.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FcFFCx0aQAIq-Il.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FcFFDbuaAAEACjy.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FcFFGgJaAAA7lu6.jpg) ([View Tweet](https://twitter.com/teej_m/status/1567622153717321728))
	- It's trivial to make mistakes when writing a funnel query - I wrote dozens of bugs in the 20+ implementations I made for this talk. You should start with a JOIN because it's simple.
	  
	  Unfortunately, it's slow. It scales poorly to data size, and stinks for 2+ steps. ([View Tweet](https://twitter.com/teej_m/status/1567622158029041664))
	- But we have a viable alternative: window functions!
	  
	  This example, like the join, is a two step funnel (step A then step B, A>B)
	  
	  A clever use of the LAG window function, lets me identify any step B with a step A before it that matches our funnel constraints. 
	  
	  ![](https://pbs.twimg.com/media/FcFHHX2agAEE6z-.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FcFHJ4xakAIfKCH.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FcFHMxoaIAAMnEE.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FcFHUJ5aAAAG4A6.jpg) ([View Tweet](https://twitter.com/teej_m/status/1567622164463108097))
	- Window functions are fast and outperformed joins on my synthetic dataset.
	  
	  Unfortunately, writing the SQL for more complex, multi-step funnels gets messy. While outperforming JOINs, they still break down under large scales of data. ([View Tweet](https://twitter.com/teej_m/status/1567622168359616512))
	- Window functions and joins share a complication: under the hood, they both effectively perform a range join. This is like a nested loop, scanning your dataset multiple times and exploding intermediate result sets. 
	  
	  ![](https://pbs.twimg.com/media/FcFJJCfaMAEU4ee.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FcFJOT9aMAAR4Od.jpg) ([View Tweet](https://twitter.com/teej_m/status/1567622173430546432))
	- There's another way: regular expressions (regex)
	  
	  In this approach, we aggregate our event data into sequence strings. A well-crafted regex then checks for funnel completion at each step.
	  
	  This forces a compromise on your time constraints, but the speedup is often worth it. 
	  
	  ![](https://pbs.twimg.com/media/FcFMzYiagAAT2E8.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FcFM28IagAA6SVZ.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FcFM_mUaQAEbupG.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FcFNB0waIAELogW.jpg) ([View Tweet](https://twitter.com/teej_m/status/1567622181110321153))
	- The regex approach has two secrets to its performance.
	  
	  First, it performs a single scan over your dataset, you don't add additional scans as your funnel adds steps.
	  
	  Second, it takes advantage of the highly optimized pattern matching routines present in most regex systems. ([View Tweet](https://twitter.com/teej_m/status/1567622185103298562))
	- So the join is slow...
	  Windows are better, but messy...
	  Regex saves the day, but at the cost of constraints...
	  
	  What else is there, you ask? ([View Tweet](https://twitter.com/teej_m/status/1567622186940403713))
	- A user-defined table function (UDTF).
	  
	  I wrote a streaming, funnel counting implementation in javascript using a UDTF.
	  
	  "It can't possibly be performant to do this in JS over highly optimized C++ code!" you cry.
	  
	  At 1B+ rows, my low-memory single-scan UDTF beats the rest easily. 
	  
	  ![](https://pbs.twimg.com/media/FcFOJL7acAArWLU.jpg) ([View Tweet](https://twitter.com/teej_m/status/1567622191830941697))
	- So that's the talk!
	  
	  In Snowflake, there are many ways you can do funnel analysis in SQL.
	- All the code and slides are available on Github
	  
	  https://t.co/DAhWSkrbSn ([View Tweet](https://twitter.com/teej_m/status/1567622204954939392))
	- P.S. - What about MATCH_RECOGNIZE? https://t.co/Q6paAGr4bP ([View Tweet](https://twitter.com/teej_m/status/1567622206703935488))