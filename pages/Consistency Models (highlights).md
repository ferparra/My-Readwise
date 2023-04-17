title:: Consistency Models (highlights)
author:: [[arXiv.org]]
full-title:: "Consistency Models"
category:: #articles
url:: https://arxiv.org/abs/2303.01469/

- Highlights first synced by [[Readwise]] [[Apr 16th, 2023]]
	- Diffusion models have made significant breakthroughs in image, audio, and video generation, but they depend on an iterative generation process that causes slow sampling speed and caps their potential for real-time applications. To overcome this limitation, we propose consistency models, a new family of generative models that achieve high sample quality without adversarial training. They support fast one-step generation by design, while still allowing for few-step sampling to trade compute for sample quality. They also support zero-shot data editing, like image inpainting, colorization, and super-resolution, without requiring explicit training on these tasks. Consistency models can be trained either as a way to distill pre-trained diffusion models, or as standalone generative models. Through extensive experiments, we demonstrate that they outperform existing distillation techniques for diffusion models in one- and few-step generation. For example, we achieve the new state-of-the-art FID of 3.55 on CIFAR-10 and 6.20 on ImageNet 64x64 for one-step generation. When trained as standalone generative models, consistency models also outperform single-step, non-adversarial generative models on standard benchmarks like CIFAR-10, ImageNet 64x64 and LSUN 256x256. ([View Highlight](https://read.readwise.io/read/01gy3tzqdztev9jn8ejmn1hrre))
		- **Note**: 1. What are the advantages of consistency models compared to existing generative models?
		  2. How does the one-step generation process of consistency models compare to the iterative process of diffusion models?
		  3. What are some practical applications of consistency models?