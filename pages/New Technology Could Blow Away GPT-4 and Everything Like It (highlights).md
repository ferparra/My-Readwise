title:: New Technology Could Blow Away GPT-4 and Everything Like It (highlights)
author:: [[ycombinator.com]]
full-title:: "New Technology Could Blow Away GPT-4 and Everything Like It"
category:: #articles
url:: https://news.ycombinator.com/item?id=35656597
tags:: #[[ai]]

- Highlights first synced by [[Readwise]] [[Apr 22nd, 2023]]
	- Notes from quick read of paper at [https://arxiv.org/abs/2302.10866](https://arxiv.org/abs/2302.10866). Title of popsci is overreaching, this is a drop-in subquadratic replacement for attention. Could be promising, but to be seen if it is adopted in practice. skybrian ([https://news.ycombinator.com/item?id=35657983](https://news.ycombinator.com/item?id=35657983)) points out new blog post by authors, and prev discussion of older (march 28th) blog post. Takeaways:
	  
	  * In standard attention in transformers, cost scales quadratically with length of sequence, which restricts model context. This work presents subquadratic exact operator allowing it to scale to larger contexts (100k+).
	  
	  * They introduce an operator called "Hyena hierarchy", a recurrence over 2 subquadratic operations: long convolution, and element-wise mul gating. Sec 3.1-3.3 define the recurrences, matrices, and filters. This is importantly, a drop in replacement for attention.
	  
	  * Longer context: 100x speedup over FlashAttention at 64k context (if we view flash attention as an non-approx engg optimization, then this work is improving algorithmically, and getting OOM over that). Associate recall, i.e., just pull data, show improvements: Experiments on 137k context, and vocab sizes of 10-40 (unsure why they have bad recall on small length sequence with larger vocab, but they still outperform others)
	  
	  * Comparisons (on relatively small models, but hoping to show pattern) with RWKV (attention-free model, trained on 332B tokens), GPTNeo (trained on 300B tokens), with Hyena trained on 137B tokens. Models are 125M-355M sized. (Section 4.3)
	  
	  * On SuperGLUE, zero-shot and 3-shot accuracy is ballpark similar to GPTNeo (although technically they underperform a bit for zero-shot and overperform a bit for 3-shot). (Table 4.5 and 4.6)
	  
	  * Because they can support large (e.g., 100k+) context, they can do image classification. They report ballpark comparable against others. (Table 4.7) ([View Highlight](https://read.readwise.io/read/01gyk1d9qnf25ergmq9b53sppw))