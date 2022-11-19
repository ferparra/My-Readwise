title:: Path Finding + Smarter A... (highlights)
author:: [[@steveruizok on Twitter]]
full-title:: "Path Finding + Smarter A..."
category:: #tweets
url:: https://twitter.com/steveruizok/status/1482391588177334275

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- path finding + smarter animations https://t.co/8fafK0NVMp ([View Tweet](https://twitter.com/steveruizok/status/1482391588177334275))
		- **Note**: Thread
	- What do I mean by smarter? Let's say each of our blocks has a position in a grid, [x, y]. (It's actually a 3D grid, so [x, y, z], but we can ignore the z for now) 
	  
	  ![](https://pbs.twimg.com/media/FJJ6SEEWYAMMz5u.png) ([View Tweet](https://twitter.com/steveruizok/status/1482391592929579011))
	- The positions map to the block's index in z/y/x arrays. This means that a block's position can only be an integer like 1 or 2, but never a float like 1.25 or 2.81. 
	  
	  So a position like [0, 0] is fine but [0.5, 0] is not. 
	  
	  ![](https://pbs.twimg.com/media/FJJ8Wv-WQAM7Tka.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1482391598503768071))
	- However, in order to animate between positions we need to interpolate that position, right? 
	  
	  ![](https://pbs.twimg.com/media/FJJ82q6XwAE54WW.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1482391603901829120))
	- The (very old) trick is to give the block an "offset" and then find the block's "draw position" by adding the two together. In the image below, both blocks have the same "position" but the one on the right has an offset that causes it to "draw" at a different place. 
	  
	  ![](https://pbs.twimg.com/media/FJJ-CGNWQAErDT1.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1482391608230359047))
	- So to animate a block, the process is: 
	  1) move the block to its new position, 
	  2) set its offset so that it draws at its old position... 
	  
	  ![](https://pbs.twimg.com/media/FJJ_T8PWQAA0HP-.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1482391612626018308))
	- And then 3) animate the offset back to zero. 
	  
	  ![](https://pbs.twimg.com/media/FJKBAl9XMAgO5VA.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1482391618191872002))
	- Throw in some delay after each animation cycle and you've got your animating blocks! https://t.co/t305iQG1nM ([View Tweet](https://twitter.com/steveruizok/status/1482391630569160707))