title:: Transformers Are All The... (highlights)
author:: [[@DrJimFan on Twitter]]
full-title:: "Transformers Are All The..."
category:: #tweets
url:: https://twitter.com/DrJimFan/status/1605893566575820800

- Highlights first synced by [[Readwise]] [[Dec 23rd, 2022]]
	- Transformers are all the rage today. But neither DALLE nor Stable Diffusion uses Transformer for image generation. Instead, they rely on a 7-year-old, Jurassic-era neural architecture. Why? 🤷🏾‍♀️⁉️ It’s finally time for Transformer and Diffusion to join forces! Quick 🧵👇: 
	  
	  ![](https://pbs.twimg.com/media/FklHr-iXEAAz0Io.jpg) ([View Tweet](https://twitter.com/DrJimFan/status/1605893566575820800))
		- **Note**: Thread
	- U-Net was published in May 2015 and originally intended for biomedical image segmentation. It has been repurposed to be the image generation backbone for most of the SOTA diffusion models, because it’s good at mapping a high-dimensional image to another. 1/ 
	  
	  ![](https://pbs.twimg.com/media/FklHsWjWAAA5RS2.jpg) ([View Tweet](https://twitter.com/DrJimFan/status/1605893572955455489))
	- 2015 is almost prehistoric by the pace of today’s explosive AI progress. In 2020, Transformers debuted in computer vision as “ViT”, from the paper “An Image is Worth 16x16 Words” by Dosovitskiy et al. Since then, ViT has found its way into almost every vision problem. 2/ 
	  
	  ![](https://pbs.twimg.com/media/FklHstIWAAIWdc3.jpg) ([View Tweet](https://twitter.com/DrJimFan/status/1605893579271917571))
	- Transformers are general-purpose, scalable, and enjoy the attention (pun intended) of a huge swarm of grad students working on improving it. In a very recent paper “Scalable Diffusion Models with Transformers”, @billpeeb & @sainingxie proposed Diffusion Transformer (DiT). 3/ https://t.co/yYjsHeeXW7 ([View Tweet](https://twitter.com/DrJimFan/status/1605893662000369665))
	- Turns out there’s nothing magical about U-Net for text-to-image. Transformers work even better with the right tricks! The authors find that the way we do label conditioning is crucial, and Adaptive LayerNorm works the best (i.e. the label embedding modulates the activations). 4/ 
	  
	  ![](https://pbs.twimg.com/media/FklHx7sX0AIEB9w.jpg) ([View Tweet](https://twitter.com/DrJimFan/status/1605893667947831296))
	- Just like all other transformers, DiT ships with the gift of a smooth scalability curve over parameters and FLOPs! The best model “DiT-XL/2” is more compute-efficient and achieves better generation quality than all prior U-Net-based diffusion models. 5/ 
	  
	  ![](https://pbs.twimg.com/media/FklHyPAXoAA-nLQ.jpg) ([View Tweet](https://twitter.com/DrJimFan/status/1605893673794822145))
	- For now, DiTs are not conditioned on natural language. The models are only able to generate ImageNet-style pictures given a class category label. But it isn’t hard to adapt the label input to be any vector, including text embeddings. Stable-DiT is just around the corner! 6/ 
	  
	  ![](https://pbs.twimg.com/media/FklHylwWIAQDHKy.jpg) ([View Tweet](https://twitter.com/DrJimFan/status/1605893683429220357))
	- The paper contains a lot more details and experiments. 
	  Website: https://t.co/ohcHEQLGFm
	  Arxiv: https://t.co/M1UfFiEn0C
	  Authors: @billpeeb (Berkeley) & @sainingxie (NYU)
	  Follow me for more paper spotlights like this! 🙌
	  END/🧵 ([View Tweet](https://twitter.com/DrJimFan/status/1605893688357318662))