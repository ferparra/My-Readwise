title:: Why Don’t More People Kn... (highlights)
author:: [[@docmilanfar on Twitter]]
full-title:: "Why Don’t More People Kn..."
category:: #tweets
url:: https://twitter.com/docmilanfar/status/1592384165298995200

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Why don’t more people know about the gem that is Tweedie's formula?
	  
	  Say 𝐱 is a noisy measurement of 𝐮
	  
	  𝐱 = 𝐮 + 𝐞
	  
	  w/ 𝐞 ∼ 𝒩(𝟎, σ² 𝐈)
	  
	  min mean² estimate of 𝐮 is 𝔼 [𝐮 | 𝐱]. Obviously we need the density P(𝐮|𝐱) right?
	  
	  No! Tweedie says P(𝐱) is all you need!
	  
	  1/2 
	  
	  ![](https://pbs.twimg.com/media/FhlI9ZCUoAASKEC.jpg) ([View Tweet](https://twitter.com/docmilanfar/status/1592384165298995200))
		- **Note**: Thread
	- If you pay attention, Tweedie appears in many ML works
	  
	  Since no need for P(𝐮|𝐱), you can model or sample the marginal P(𝐱) directly
	  
	  ∇P(𝐱)/P(𝐱) = ∇logP(𝐱) means MMSE is a gradient step ala Langevin:  𝐱' = 𝐱 - a ∇ logP(𝐱) 
	  
	  Motivates denoising diffusion score-matching 
	  
	  ![](https://pbs.twimg.com/media/FhlJhj8VEAAForE.jpg) ([View Tweet](https://twitter.com/docmilanfar/status/1592384786697695233))