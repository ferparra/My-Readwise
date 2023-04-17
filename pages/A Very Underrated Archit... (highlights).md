title:: A Very Underrated Archit... (highlights)
author:: [[@lvwerra on Twitter]]
full-title:: "A Very Underrated Archit..."
category:: #tweets
url:: https://twitter.com/lvwerra/status/1646193143535091719

- Highlights first synced by [[Readwise]] [[Apr 13th, 2023]]
	- A very underrated architecture tweak to GPT is multi-query attention (MQA): sharing value/key across attention heads saves a lot of memory in the kv-cache.
	  
	  Max generation batch size on a Colab GPU with a 1B model:❗️512❗️ vs 32 (vanilla GPT)
	  
	  Test it here: https://t.co/cla8T9TfKh ([View Tweet](https://twitter.com/lvwerra/status/1646193143535091719))
		- **Note**: Thread
	- The vanilla GPT architecture uses multi-head attention where each attention head has its own query, key, and value matrices. During generation the keys and values of previous tokens are cached to prevent re-computing them and so GPU memory usage grows with each generated token. ([View Tweet](https://twitter.com/lvwerra/status/1646193145560940554))
	- The idea of MQA is to have a single key and value that are shared across heads. A big model can have up to 96 heads (such as GPT-3) which means using MQA can save 96x the memory consumption of the key/value cache. 
	  
	  Paper: https://t.co/i2EsElrmi8 ([View Tweet](https://twitter.com/lvwerra/status/1646193147565817859))
	- That's especially interesting for applications that require a lot of text generation such as code evaluation or RLHF where generation can become a bottleneck! 
	  
	  No surprise that both PaLM and AlphaCode used it. ([View Tweet](https://twitter.com/lvwerra/status/1646193149662969875))
	- SantaCoder is (afaik) the first open source model applying MQA.
	  
	  Give it a shot here: https://t.co/iswkaWXMzW ([View Tweet](https://twitter.com/lvwerra/status/1646193151328002054))