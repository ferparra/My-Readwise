title:: Attention Is All You Need: Discovering the Transformer Paper (highlights)
author:: [[Eduardo Muñoz]]
full-title:: "Attention Is All You Need: Discovering the Transformer Paper"
category:: #articles
url:: https://towardsdatascience.com/attention-is-all-you-need-discovering-the-transformer-paper-73e5ff5e0634
tags:: #[[language models]] #[[tensorflow]] #[[transformers]]

- Highlights first synced by [[Readwise]] [[Jan 23rd, 2023]]
	- In sequence-to-sequence problems such as the neural machine translation, the initial proposals were based on the use of RNNs in an encoder-decoder architecture. These architectures have a great limitation when working with long sequences, their ability to retain information from the first elements was lost when new elements were incorporated into the sequence. ([View Highlight](https://read.readwise.io/read/01gqehjvjd67dgqjcsb6dh8pds))
		- **Tags**: #[[neural networks]] #[[rnns]]
	- This is what attention does, it extracts information from the whole sequence, a **weighted sum of all the past encoder states**. This allows the decoder to assign greater weight or importance to a certain element of the input for each element of the output. ([View Highlight](https://read.readwise.io/read/01gqehkwf4zyr1x0jxyr3fsvd2))
	- In this work we propose the Transformer, a model architecture eschewing recurrence and instead relying entirely on an attention mechanism to draw global dependencies between input and output. The Transformer allows for significantly more parallelization … the Transformer is the first transduction model relying entirely on self-attention to compute representations of its input and output without using sequence-aligned RNNs or convolution.
	  
	  “Attention is all you need” paper [1] ([View Highlight](https://read.readwise.io/read/01gqehmms7r3t983dm25etjs3y))
	- ![](https://miro.medium.com/max/428/1*ZCFSvkKtppgew3cc7BIaug.png) ([View Highlight](https://read.readwise.io/read/01gqehne9aejsqqa5pjhr99q6k))
	- Self-attention is a sequence-to-sequence operation: a sequence of vectors goes in, and a sequence of vectors comes out. Let’s call the input vectors `x1`, `x2`,…, `xt` and the corresponding output vectors `y1`, `y2`,…, `yt`. The vectors all have dimension k. To produce output vector `yi`, the self attention operation simply takes *a weighted average over all the input vectors,* the simplest option is the dot product.
	  
	  [Transformers from scratch by Peter Bloem](http://peterbloem.nl/blog/transformers) [2] ([View Highlight](https://read.readwise.io/read/01gqehnxam3wrakpxe0g5ttfcw))
	- ![](https://miro.medium.com/max/700/1*r6S_FHm9h82w1hDnpyaHeA.png) ([View Highlight](https://read.readwise.io/read/01gqehp1xe18d6zmexqmacavs4))
	- To this end, we add “positional encodings” to the input embeddings at the bottoms of the encoder and decoder stacks. The positional encodings have the same dimension as the embeddings, so that the two can be summed. There are many choices of positional encodings.
	  
	  “Attention is all you need” paper ([View Highlight](https://read.readwise.io/read/01gqehppf1fegpbq2jc7q1t8ea))
	- *Normalization and residual connections are standard tricks used to help deep neural networks train faster and more accurately. The layer normalization is applied over the embedding dimension only.*
	  
	  Peter Bloem, “Transformers from scratch” [2] ([View Highlight](https://read.readwise.io/read/01gqehpypmhcfjkg1qyez6r510))
		- **Tags**: #[[neural networks]] #[[normalization]]
	- ![](https://miro.medium.com/max/692/1*y05XJlCykLUE5wPdWfVoiQ.png) ([View Highlight](https://read.readwise.io/read/01gqehqs5h0xvtr2prh6yqfcyc))
	- ![](https://miro.medium.com/max/700/1*zuBmEZDoS2WvNRfIACwrCA.png) ([View Highlight](https://read.readwise.io/read/01gqehr09en8c1p9b9100y7tzh))