title:: New Method for LLM Quantization (highlights)
author:: [[W&B]]
full-title:: "New Method for LLM Quantization"
category:: #articles
url:: https://wandb.ai/byyoung3/ml-news/reports/New-Method-For-LLM-Quantization--VmlldzozOTU1NTgz

- Highlights first synced by [[Readwise]] [[Apr 16th, 2023]]
	- Quantization is a well-studied method for making neural networks more efficient. As neural nets grow in size, the cost to run the model grows, the memory required to store the model weights also grows, and the result is higher costs for compute, especially in LLMs that contain billions of parameters. ([View Highlight](https://read.readwise.io/read/01gy4dbenmzq104tqtx9kbfpv8))
	- SmoothQuant essentially proposes to “smooth” the input activation by a smoothing factor. The division by the smoothing factor is then reversed by multiplying the smoothing factor by the weights, which results in an equivalent operation as before while making the activations quantizable. ([View Highlight](https://read.readwise.io/read/01gy4df9ndyy8x77f0hmq2cbn4))