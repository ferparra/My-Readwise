title:: What Is a Transformer Model? (highlights)
author:: [[Rick Merritt]]
full-title:: "What Is a Transformer Model?"
category:: #articles
url:: https://blogs.nvidia.com/blog/2022/03/25/what-is-a-transformer-model/
document_note:: Transformer models are a class of neural networks that use attention or self-attention to detect subtle relationships between data elements in a sequence. They are being used for a variety of applications such as translation, fraud detection, manufacturing, online recommendations, and healthcare. Transformers eliminate the need for large, labeled datasets and offer parallel processing capabilities, enabling them to generate accurate predictions and create better models. Google's 2017 paper on transformers marked the beginning of the "transformer AI" era. The NVIDIA H100 GPU can accelerate transformer training and inference.
tags:: #[[transformers]]

- Highlights first synced by [[Readwise]] [[Mar 28th, 2023]]
	- A transformer model is a neural network that learns context and thus meaning by tracking relationships in sequential data like the words in this sentence. ([View Highlight](https://read.readwise.io/read/01gwdhp25b4h52kmtb16qe460n))
	- ![](https://blogs.nvidia.com/wp-content/uploads/2022/03/Transformer-apps-672x459.jpg) ([View Highlight](https://read.readwise.io/read/01gwdhpg9qvzfda6fhdemfjpbt))
	- Transformers are in many cases replacing convolutional and recurrent neural networks (CNNs and RNNs), the most popular types of deep learning models just five years ago. ([View Highlight](https://read.readwise.io/read/01gwdhpz46x84qbmgfshc4pgh8))
	- ![](https://blogs.nvidia.com/wp-content/uploads/2022/03/Transformer-model-example-aidan-gomez-672x400.jpg) ([View Highlight](https://read.readwise.io/read/01gwdhq34w0r9sxczjee4jrgjq))
	- **Self-Attention Finds Meaning**
	  
	  For example, in the sentence:
	  
	  *She poured water from the pitcher to the cup until it was full.*
	  
	  We know “it” refers to the cup, while in the sentence:
	  
	  *She poured water from the pitcher to the cup until it was empty.*
	  
	  We know “it” refers to the pitcher.
	  
	  “Meaning is a result of relationships between things, and self-attention is a general way of learning relationships,” said Ashish Vaswani, a former senior staff research scientist at Google Brain who led work on the seminal 2017 paper. ([View Highlight](https://read.readwise.io/read/01gwdhr2pp72gydnpw968fa3fs))