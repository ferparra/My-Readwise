title:: So @StableDiffusion Has... (highlights)
author:: [[@iScienceLuvr on Twitter]]
full-title:: "So @StableDiffusion Has..."
category:: #tweets
url:: https://twitter.com/iScienceLuvr/status/1564847717066559488

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- So @StableDiffusion has various options and controls and one of the main ones is the sampler used for generation. Let's talk a little bit about these samplers since this has some interesting and unexpected effects on generated image quality (below image from subreddit)🧵 
	  
	  ![](https://pbs.twimg.com/media/Fbd0s-tVUAAjv5e.png) ([View Tweet](https://twitter.com/iScienceLuvr/status/1564847717066559488))
		- **Note**: Thread
	- First, a brief summary about how Stable Diffusion works. Stable Diffusion is a diffusion model, which is a neural network trained to iteratively denoise an image from pure noise. (2/11) 
	  
	  ![](https://pbs.twimg.com/media/Fbd0tbTVQAEzxiD.png) ([View Tweet](https://twitter.com/iScienceLuvr/status/1564847724033241088))
	- This works since learning to denoise images requires you to understand how those images are composed and how to generate parts of the image to replace and fix the noise. 
	  
	  Typically these models work on pixels and directly produce RGB images but not Stable Diffusion! (3/11) ([View Tweet](https://twitter.com/iScienceLuvr/status/1564847726860218371))
	- Stable Diffusion is a *latent* diffusion model, meaning images are represented by low-dimensional embedding, and the diffusion model works with these and produces a latent embedding that maps to our generated image (using an autoencoder). (4/11) 
	  
	  ![](https://pbs.twimg.com/media/Fbd0t8IUcAAjovP.png) ([View Tweet](https://twitter.com/iScienceLuvr/status/1564847733944377345))
	- Since this is working with these smaller latent embeddings, *latent* diffusion models help alleviate some of the notorious computational inefficiencies of diffusion models. (5/11) ([View Tweet](https://twitter.com/iScienceLuvr/status/1564847737740308481))
	- Now a key aspect relating to samplers is that this iterative application of our denoising neural network is equivalent to a discretized differential equation. So all these samplers that you see here are mostly just fancy ways of solving these differential equations! (6/11) 
	  
	  ![](https://pbs.twimg.com/media/Fbd0ukTUUAAcT_E.png) ([View Tweet](https://twitter.com/iScienceLuvr/status/1564847743180296192))
	- Here is a technical summary I wrote up of the different samplers.
	  
	  Basically, the DDIM & PLMS samplers were originally part of the Latent Diffusion repository.
	  
	  The k-samplers come from @RiversHaveWings's amazing k-diffusion repo (give it a star!): https://t.co/cvVCcQnBQW (7/11) 
	  
	  ![](https://pbs.twimg.com/media/Fbd0u6LUIAAdbnv.png) ([View Tweet](https://twitter.com/iScienceLuvr/status/1564847749073276928))
	- Now here's something interesting regarding these samplers. Folks have observed amazing results with one sampler: k_euler_ancestral. Even more interesting is that it only requires about 5-10 steps to get decent results! (image by @Arman_point0)
	  
	  This is actually quite odd! (8/11) 
	  
	  ![](https://pbs.twimg.com/media/Fbd0vRlUcAADkoH.png) ([View Tweet](https://twitter.com/iScienceLuvr/status/1564847756421656576))
	- k_euler_ancestral should be the worst! It's the most basic sampler, based on the original diffusion model (DDPM). It usually takes 100s of steps to get good images, not 5! The other samplers are newer & more sophisticated to sample faster & generate higher quality images. (9/11) ([View Tweet](https://twitter.com/iScienceLuvr/status/1564847759332495361))
	- This puzzled me when I looked into this & I think it also puzzled @RiversHaveWings a bit.
	  
	  Maybe these sophisticated samplers are better for diffusion models on direct RGB images, but when working with latent embeddings, few steps are enough to map to a decent RGB image. (10/11) ([View Tweet](https://twitter.com/iScienceLuvr/status/1564847761895280640))
	- There is something about how samplers interact with latent diffusion models that is probably not well-understood right now and could be an interesting direction of research! 
	  
	  If anyone has any thoughts on this, let me know! (11/11) ([View Tweet](https://twitter.com/iScienceLuvr/status/1564847764424388608))