title:: 100K Context Windows (highlights)
author:: [[ycombinator.com]]
full-title:: "100K Context Windows"
category:: #articles
url:: https://news.ycombinator.com/item?id=35904773

- Highlights first synced by [[Readwise]] [[May 15th, 2023]]
	- This is the first time I've felt like Anthropic may be a true competitor to OpenAI.
	  
	  I see 6 ways to improve foundation LLMs other than cost. If your product is best at one of the below, and has parity at the other 5 items, then customers will switch. I'm currently using GPT-4-8k. I regularly run into the context limit. If Claude-100K is close enough on "intelligence" then I will switch.
	  
	  Six Dimensions to Compare Foundation LLMs:
	  
	  1. Smarter models
	  
	  2. Larger context windows
	  
	  3. More input and output modes
	  
	  4. Lower time to first response token and to full response
	  
	  5. Easier prompting
	  
	  6. Integrations ([View Highlight](https://read.readwise.io/read/01h06p8fdmgpagb057xca8httx))
	- The embeddings work only in some cases where the answer is in a short part(s) of the document. If user asks something like "what are the main ideas?" or "Summarize the document." or any question that needs context from large portions of the book/pdf/file, then it will not work with the embeddings trick that use just short passages in prompt. But if large context windows costs are high, we need to keep using embeddings and few text parts. ([View Highlight](https://read.readwise.io/read/01h06p9t24zr21rkar0hm9kfjj))
	- Can LLMs take advantage of this bigger window to solve meaningful tasks though? I can't imagine in the training data, knowing what happened 100k tokens ago would be _that_ relevant to predicting the current token very often, so unless this is something that the model learns to leverage more implicitly, I'd be a bit pessimistic.
	  
	  [reply](https://news.ycombinator.com/item?id=35904773/reply&id=35905396&goto=item%3Fid%3D35904773%2335905396)
	  
	  ![](https://news.ycombinator.com/item?id=35904773/s.gif)
	  
	  [
	  
	  ](https://news.ycombinator.com/item?id=35904773/vote&id=35905498&how=up&goto=item%3Fid%3D35904773)
	  
	  [ttul](https://news.ycombinator.com/item?id=35904773/user&id=ttul) [6 hours ago](https://news.ycombinator.com/item?id=35904773/item&id=35905498) | [parent](https://news.ycombinator.com/item?id=35904773#35905396) | [next](https://news.ycombinator.com/item?id=35904773#35906297) [[–]](javascript:void(0))
	  
	  
	  
	  Yes. For instance, a large context window allows you to have a chat for months where the model can remember and make use of everything you’ve ever talked about. That enables creating a much more effective “assistant” that can remember key details months later that may be valuable.
	  
	  A second example is the analysis of long documents. Today, hacks like chunking and HyDE enable us to ask questions about a long document or a corpus of documents. But is far superior if the model can ingest the whole document and apply attention to everything, rather than just one chunk at a time. Chunking effectively means that the model is limited to drawing conclusions from one chunk at a time and cannot synthesize useful responses relating to the entire document. ([View Highlight](https://read.readwise.io/read/01h06peqkjnstycj87s7p1fa1d))