title:: Why Donโt More People Kn... (highlights)
author:: [[@docmilanfar on Twitter]]
full-title:: "Why Donโt More People Kn..."
category:: #tweets
url:: https://twitter.com/docmilanfar/status/1592384165298995200

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Why donโt more people know about the gem that is Tweedie's formula?
	  
	  Say ๐ฑ is a noisy measurement of ๐ฎ
	  
	  ๐ฑ = ๐ฎ + ๐
	  
	  w/ ๐ โผ ๐ฉ(๐, ฯยฒ ๐)
	  
	  min meanยฒ estimate of ๐ฎ is ๐ผ [๐ฎ | ๐ฑ]. Obviously we need the density P(๐ฎ|๐ฑ) right?
	  
	  No! Tweedie says P(๐ฑ) is all you need!
	  
	  1/2 
	  
	  ![](https://pbs.twimg.com/media/FhlI9ZCUoAASKEC.jpg) ([View Tweet](https://twitter.com/docmilanfar/status/1592384165298995200))
		- **Note**: Thread
	- If you pay attention, Tweedie appears in many ML works
	  
	  Since no need for P(๐ฎ|๐ฑ), you can model or sample the marginal P(๐ฑ) directly
	  
	  โP(๐ฑ)/P(๐ฑ) = โlogP(๐ฑ) means MMSE is a gradient step ala Langevin:  ๐ฑ' = ๐ฑ - a โ logP(๐ฑ) 
	  
	  Motivates denoising diffusion score-matching 
	  
	  ![](https://pbs.twimg.com/media/FhlJhj8VEAAForE.jpg) ([View Tweet](https://twitter.com/docmilanfar/status/1592384786697695233))