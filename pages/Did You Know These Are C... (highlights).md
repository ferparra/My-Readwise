title:: Did You Know These Are C... (highlights)
author:: [[@DanHollick on Twitter]]
full-title:: "Did You Know These Are C..."
category:: #tweets
url:: https://twitter.com/DanHollick/status/1587812691355107329

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Did you know these are called Boolean Operations?
	  
	  That's because they use booleans to determine which part of the shapes should be visible.
	  
	  Let me explain 👇 
	  
	  ![](https://pbs.twimg.com/media/FgkLOj-UcAARsYd.png) ([View Tweet](https://twitter.com/DanHollick/status/1587812691355107329))
		- **Note**: Thread
	- To keep it simple lets use two overlapping circles.
	  
	  Imagine a boolean for each circle called "inside" - for the area inside each circle the boolean is true, for the area outside it is false.
	  
	  Any point within the bounding box can be represented in terms of these booleans. 
	  
	  ![](https://pbs.twimg.com/media/FgkLO3qUcAEiE1f.png) ([View Tweet](https://twitter.com/DanHollick/status/1587812698992959488))
	- Boolean operations are just a way of combining these booleans together to make a new shape.
	  
	  Take Union for example- the new shape will consist of any area that is inside the red circle OR the blue circle. 
	  
	  ![](https://pbs.twimg.com/media/FgkLPTXUcAIv78L.png) ([View Tweet](https://twitter.com/DanHollick/status/1587812706324647936))
	- Because we have combined the two booleans, there are now 4 possible states (2x2) :
	- You can see this more clearly with Intersect which creates a new shape where the two shapes overlap.
	  
	  Put differently, anywhere "inside" is true for BOTH shapes. 
	  
	  ![](https://pbs.twimg.com/media/FgkLQHuUcAAbK4f.jpg) ([View Tweet](https://twitter.com/DanHollick/status/1587812720086110209))
	- Difference/Exclude is almost the inverse of the Intersect.
	  
	  It creates a shape anywhere "inside" is true for one but NOT BOTH of the shapes. 
	  
	  ![](https://pbs.twimg.com/media/FgkLQgWVIAAfqIG.png) ([View Tweet](https://twitter.com/DanHollick/status/1587812727140995073))
	- Subtract works differently in that it matters which shape is the primary shape. In Figma's case the top layer is subtracted from the bottom.
	  
	  The new shape is anywhere "inside" is true for the primary shape AND NOT the secondary shape 
	  
	  ![](https://pbs.twimg.com/media/FgkLQ8vVsAA0PZr.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FgkLRKwVUAEsnWV.jpg) ([View Tweet](https://twitter.com/DanHollick/status/1587812738335531009))
	- This example is pretty simple but Boolean Operations are extremely powerful and work on complex shape combinations.
	  
	  The math required to determine the overlapping areas of complex shapes deserves a whole thread on its own. 
	  
	  ![](https://pbs.twimg.com/media/FgkLRlYUAAEdrXX.jpg) ([View Tweet](https://twitter.com/DanHollick/status/1587812745025495041))
	- If you think these operations look familiar it's because they are essentially the logical operators we use in programming:
	  
	  AND - Intersect
	  OR - Union
	  NAND - Exclusion (kinda of)
	  NOT - Subtract (kind of) ([View Tweet](https://twitter.com/DanHollick/status/1587812748133474306))
	- Wanna play with vector boolean operations? Check out paper.js which has some really helpful primitives for this.
	  
	  https://t.co/OFNSLaYfqc https://t.co/larHxAE8mw ([View Tweet](https://twitter.com/DanHollick/status/1587812770229063681))
	- //TODO: write something clever that gets you to retweet the original tweet. https://t.co/PxoGFMpOpO ([View Tweet](https://twitter.com/DanHollick/status/1587812773576122369))
	- You can read the unrolled version of this thread here: https://t.co/5DASjuKDfh ([View Tweet](https://twitter.com/DanHollick/status/1587812776243695616))