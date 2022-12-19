title:: Here's a Peek Behind Cau... (highlights)
author:: [[@lukaskoebis on Twitter]]
full-title:: "Here's a Peek Behind Cau..."
category:: #tweets
url:: https://twitter.com/lukaskoebis/status/1485944221169520645

- Highlights first synced by [[Readwise]] [[Dec 4th, 2022]]
	- Here's a peek behind Causal's multi-dimensional spreadsheet calculation engine — a thread (for engineers) 👇 (1/9) https://t.co/g3URx1oBJo ([View Tweet](https://twitter.com/lukaskoebis/status/1485944221169520645))
		- **Note**: Thread
	- Causal is similar to Excel, with 3 core differences:
	  (a) instead of cells, you work with "variables" and write plain-English formulas like "Profit = Revenue - Cost"; (2/9) https://t.co/pKr3DmZqLY ([View Tweet](https://twitter.com/lukaskoebis/status/1485944238466600960))
	- (b) input variables can be uncertain (e.g. "10% to 20%") and Causal runs Monte-Carlo simulations to calculate the probability distributions of output variables; (3/9) 
	  
	  ![](https://pbs.twimg.com/media/FJ8fuTRWQAgluSZ.jpg) ([View Tweet](https://twitter.com/lukaskoebis/status/1485944242392469509))
	- (c) variables can have dimensions (e.g. Revenue might be broken down by Product, Geography, and Time) and Causal automatically performs its calculations across all dimensions. Example: (4/9) 
	  
	  ![](https://pbs.twimg.com/media/FJ8h5mXXEAAx9X6.png) ([View Tweet](https://twitter.com/lukaskoebis/status/1485944245928218627))
	- Let's say you have 1000 products, 10 geographies, 10*52 weeks, and want to run 100 Monte-Carlo samples. 
	  
	  That means just for a single variable we have to execute 520M operations. (5/9) ([View Tweet](https://twitter.com/lukaskoebis/status/1485944248524587011))
	- Our first calculation engine was implemented in Typescript and ran in the browser. 
	  
	  After frying people's laptops we moved it over to Nod which was able to handle ~1M cells. (6/9) ([View Tweet](https://twitter.com/lukaskoebis/status/1485944250269372418))
	- The next iteration was a rewrite in Golang that sped up our engine by an order of magnitude by parallelising the calculations and having more control over memory allocations. (7/9) ([View Tweet](https://twitter.com/lukaskoebis/status/1485944251880034306))
	- Currently, we can handle models with millions of cells, but our customers will soon need billions. 
	  
	  To get there we have to improve our in-memory cache, optimise our multi-dimensional data structures, compute the minimal set of numbers to render what the user requests, etc (8/9) ([View Tweet](https://twitter.com/lukaskoebis/status/1485944253687775235))
	- We're hiring engineers to work on this system and other novel + challenging problems: https://t.co/LAGdhwMIer
	  
	  If this sounds interesting, I'd love to chat! lukas@causal.app / DMs open (9/9) ([View Tweet](https://twitter.com/lukaskoebis/status/1485944255436759042))