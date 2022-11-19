title:: Basic Fact All Graphics... (highlights)
author:: [[@keenanisalive on Twitter]]
full-title:: "Basic Fact All Graphics..."
category:: #tweets
url:: https://twitter.com/keenanisalive/status/1529490555893428226

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Basic fact all graphics coders should know:
	  
	  To uniformly sample points in a disk, you'd think you could just pick a random radius r ∈ [0,1] and a random angle θ ∈ [0,2π] to generate points r (cos θ, sin θ).
	  
	  This doesn't work!
	  
	  …But take the square root of r, and it does! 1/3 
	  
	  ![](https://pbs.twimg.com/media/FTnXYcGXwAEe3Ch.jpg) ([View Tweet](https://twitter.com/keenanisalive/status/1529490555893428226))
		- **Note**: Thread
	- Intuitively: in the first formula, there are about as many points concentrated in a small annulus around the middle as there are in a large outer annulus.
	  
	  The second formula effectively corrects for the circumference of the annulus, by "warping" samples in the r direction. 2/3 
	  
	  ![](https://pbs.twimg.com/media/FTnXbbqWYAQS0sm.jpg) ([View Tweet](https://twitter.com/keenanisalive/status/1529490562088411138))
	- This formula—and a general recipe for uniformly sampling from 2-dimensional shapes—can be found in the excellent article,
	  
	  Jim Arvo
	  "Stratified Sampling of 2-Manifolds"
	  SIGGRAPH Course Notes (2001)
	  
	  https://t.co/KwajsOrze9
	  3/3 
	  
	  ![](https://pbs.twimg.com/media/FTnXgV8WIAYf_-J.png) ([View Tweet](https://twitter.com/keenanisalive/status/1529490568639823872))