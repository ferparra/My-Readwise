title:: Here's a Simple (&Lt; 10... (highlights)
author:: [[@RLanceMartin on Twitter]]
full-title:: "Here's a Simple (&Lt; 10..."
category:: #tweets
url:: https://twitter.com/RLanceMartin/status/1631716052194430976

- Highlights first synced by [[Readwise]] [[Mar 6th, 2023]]
	- Here's a simple (< 100 lines of code) app to run #ChatGPT question-answering on any uploaded document (using @LangChainAI DBQA w/ ChatGPT API): https://t.co/dGGY69YHDz 
	  
	  ![](https://pbs.twimg.com/media/FqT-JoEagAE-kNa.jpg) ([View Tweet](https://twitter.com/RLanceMartin/status/1631716052194430976))
		- **Note**: Thread
	- Uses @andrewwhite01 paper-qa reader; found this better than @LangChainAI PagedPDFSplitter, but sensitivity of response to split size (esp on larger docs). @rachel_l_woods and @hwchase17 address this in recent pod. Curious abt best practice. 
	  
	  ![](https://pbs.twimg.com/media/FqT-x7kaAAAvrr-.jpg) ([View Tweet](https://twitter.com/RLanceMartin/status/1631716054606155776))
	- Overall flow follows steps below. On longer docs (contracts, building codes), have seen best results w/ 4k split size, but can run into ChatGPT's 4096 token context length ...    https://t.co/XqZYRyHpRH ([View Tweet](https://twitter.com/RLanceMartin/status/1631716056892067841))
	- ... code below; welcome improvements, esp on doc splitting. Also like @trychroma for VectorDB (this is using FAISS, but performance similar AFAICT) https://t.co/3ABAt0DbSM ([View Tweet](https://twitter.com/RLanceMartin/status/1631716058339090432))
	- Finally, good general discussion on DBQA theme w/ @atroyn and @eriktorenberg: reduce hallucination, use LLM as compute / synthesis on top of narrow corpus / index. Many uses-cases (e.g., contracts, internal docs, local govt, etc) https://t.co/pDe7ch0wJN  https://t.co/Fui43RwnRl ([View Tweet](https://twitter.com/RLanceMartin/status/1631716059542851584))