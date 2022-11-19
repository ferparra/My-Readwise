title:: Diffusion Models Like #D... (highlights)
author:: [[@tomgoldsteincs on Twitter]]
full-title:: "Diffusion Models Like \#D..."
category:: #tweets
url:: https://twitter.com/tomgoldsteincs/status/1562503814422630406

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Diffusion models like #DALLE and #StableDiffusion are state of the art for image generation, yet our understanding of them is in its infancy. This thread introduces the basics of how diffusion models work, how we understand them, and why I think this understanding is broken.🧵 
	  
	  ![](https://pbs.twimg.com/media/Fa5mN9VWIAApbKN.png) ([View Tweet](https://twitter.com/tomgoldsteincs/status/1562503814422630406))
		- **Note**: Thread
	- Diffusion models are powerful image generators, but they are built on two simple components:  a function that degrades images by adding Gaussian noise, and a simple image restoration network for removing this noise. 
	  
	  ![](https://pbs.twimg.com/media/Fa5pv6dXwAA9Le0.png) ([View Tweet](https://twitter.com/tomgoldsteincs/status/1562503816679145474))
	- We create training data for the restoration network by adding Gaussian noise to clean images. The model accepts a noisy image as input and spits out a cleaned image.  We train by minimizing a loss that measures the L1 difference between the original image and the denoised output. 
	  
	  ![](https://pbs.twimg.com/media/Fa72GQzWIAAlXTQ.jpg) ([View Tweet](https://twitter.com/tomgoldsteincs/status/1562503822748286982))
	- These denoising nets are quite powerful. In fact, they are so powerful that we can hand them an array of pure noise and they will restore it to an image. Every time we hand it a different noise array, we get back a different image. And there we have it - an image generator! 
	  
	  ![](https://pbs.twimg.com/media/Fa5cR0gXwAA9WuV.png) ([View Tweet](https://twitter.com/tomgoldsteincs/status/1562503826904870913))
	- Err….well…sort of. You may have noticed that this generator doesn't work so well.  The image looks really blurry and has no details.  This behavior is expected though because the L1 loss function is bad for severe denoising.  Here's why... ([View Tweet](https://twitter.com/tomgoldsteincs/status/1562503829421142018))
	- When a model is trained with severe noise, it can’t tell exactly where edges should be in an image. If it puts an edge in the wrong place, it will incur a large loss.  For this reason, it minimizes the loss by smoothing over ambiguous object boundaries and removing fine details. ([View Tweet](https://twitter.com/tomgoldsteincs/status/1562503831597883392))
	- Of course the severity of this over-smoothing depends on how noisy the training data is.  A model trained on mild-noise images like this one can accurately tell where object edges are located.  It learns to minimize the loss by restoring sharp edges rather than blurring them out. 
	  
	  ![](https://pbs.twimg.com/media/Fa5dEIRXkAEzgth.png) ([View Tweet](https://twitter.com/tomgoldsteincs/status/1562503836266545152))
	- So how can we generate good images? First, use a severe noise model to convert pure noise to a blurry image. Then feed this blurry image to a mild-noise model that outputs sharp images.  The mild-noise model expects noisy inputs though, so we add noise to the blurry image first. ([View Tweet](https://twitter.com/tomgoldsteincs/status/1562503838338150401))
	- Here's the process in detail:  The denoiser converts pure noise to a blurry image.  We then add some noise back to this image, and feed it to a model trained with lower noise levels, which creates a less blurry image. Add some noise back, and denoise again...and again. 
	  
	  ![](https://pbs.twimg.com/media/Fa5oWi-WIAAb-hx.png) ([View Tweet](https://twitter.com/tomgoldsteincs/status/1562503842909941761))
	- We repeat this process using progressively lower noise levels until the noise is zero.  We now have a refined output image with sharp edges and features. This iteration process escapes the limitations of the Lp-norm loss on which our models were trained. 
	  
	  ![](https://pbs.twimg.com/media/Fa5ekNqX0AAqyZe.jpg) ([View Tweet](https://twitter.com/tomgoldsteincs/status/1562503847620546563))
	- What about those fancy models that make images from text descriptions, like DALLE and GLIDE and Stable Diffusion?  These use similar denoising models, but with two inputs. At train time, a clean image is degraded and handed to the denoising model for training, just like usual. ([View Tweet](https://twitter.com/tomgoldsteincs/status/1562503850350653440))
	- At the same time, a caption describing the image is pushed through a language model and converted to embedded features, which are then provided as an additional input to the denoiser.  Training and generation proceed just like before, but with text inputs providing hints. 
	  
	  ![](https://pbs.twimg.com/media/Fa5gDGeXoAAYTgG.jpg) ([View Tweet](https://twitter.com/tomgoldsteincs/status/1562503854159450112))
	- Theoreticians understand diffusion as a method for using noise to explore an image distribution.  The denoising step can be interpreted as a method for taking a noisy image and moving it closer to the natural image manifold using gradient ascent on the image density function. ([View Tweet](https://twitter.com/tomgoldsteincs/status/1562503856646684674))
	- When these denoising steps are alternated with steps that add noise, we get a classical process called Langevin Diffusion in which iterates bounce around the image distribution.  When this process runs for long enough, the iterates behave like samples from the true distribution. ([View Tweet](https://twitter.com/tomgoldsteincs/status/1562503858110115840))
	- So why is this understanding broken?  Existing theories of diffusion rely strongly on properties of Gaussian noise.  They also require a source of randomness in the image generator that slowly sweeps from a “hot” noisy phase to a “cold” deterministic phase. ([View Tweet](https://twitter.com/tomgoldsteincs/status/1562503859867910144))
	- However, my lab has recently observed that generative models can be built from any image degradation, not just noise.  Here's an example in which images are degraded using heavy synthetic snow (from ImageNet-C).  By iteratively removing and adding snow, we can restore the image. 
	  
	  ![](https://pbs.twimg.com/media/Fa5iofUWYAAhcuJ.png) ([View Tweet](https://twitter.com/tomgoldsteincs/status/1562503863890251776))
	- Snow and animorphosis (above) are fun curiosities, but in practice we might want diffusion processes for inverting real-world image degradations, like blur, pixelation, desaturation, etc.  By swapping noise with arbitrary transforms, we get diffusions that invert almost anything. 
	  
	  ![](https://pbs.twimg.com/media/Fa5juxkWIAASsAT.jpg) ([View Tweet](https://twitter.com/tomgoldsteincs/status/1562503869984559104))
	- These generalized diffusions work great, and yet they violate every existing theory of diffusion, all of which rely strongly on the use of Gaussian noise.  Some of these are even “cold” diffusions that require no source of randomness at all. 
	  https://t.co/eloW4IjFn2 ([View Tweet](https://twitter.com/tomgoldsteincs/status/1562503872383307779))
	- Appendix:  If you want to learn more, here’s a reading list that covers diffusion topics.
	  
	  Iterative denoising processes for image generation: 
	  https://t.co/2Tp61o4yfy (DDIM)
	  https://t.co/9VcK9gwap1 (DDPM)
	  https://t.co/Mg1PicBtle (Score Matching) ([View Tweet](https://twitter.com/tomgoldsteincs/status/1562503874409545730))
	- https://t.co/RMk4AXQbnj (Improved DDPM)
	  https://t.co/KyJCuE0zSn (Image restoration)
	  
	  Neural architectures for diffusion: 
	  https://t.co/YN2juO0ggz ([View Tweet](https://twitter.com/tomgoldsteincs/status/1562503875915292673))
	- Text to image models:
	  https://t.co/E4fGCMNNPg (Classifier-free guidance) 
	  https://t.co/6NseFVjt25 (The GLIDE model) 
	  https://t.co/9tYgWwsENU (Latent diffusion models) ([View Tweet](https://twitter.com/tomgoldsteincs/status/1562503877458464770))
	- Theoretical foundations:
	   https://t.co/f29Owb61ZP (Original paper by Sohl-Dickstein et al) 
	  https://t.co/dpb6hOKkZ0 (Score-based models) 
	  https://t.co/dOSIzFz72T (Gradients of data distributions) ([View Tweet](https://twitter.com/tomgoldsteincs/status/1562503879644053504))
	- Finally, thanks a bunch to @arpitbansal297
	  @EBorgnia, Hong-Min Chu, Jie Li, @hamid_kazemi22, @furongh, @micahgoldblum, and @jonasgeiping! ([View Tweet](https://twitter.com/tomgoldsteincs/status/1562508498214141953))