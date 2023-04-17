title:: LlamaIndex Provides The... (highlights)
author:: [[@jerryjliu0 on Twitter]]
full-title:: "LlamaIndex Provides The..."
category:: #tweets
url:: https://twitter.com/jerryjliu0/status/1643627275236130816

- Highlights first synced by [[Readwise]] [[Apr 7th, 2023]]
	- LlamaIndex provides the key components to easily connect/index your data for LLM use. 🗂️🛠️🧠
	  
	  Over the past two weeks we’ve made LlamaIndex much more modular and much more powerful.
	  
	  Let’s take a tour - we’d love your feedback as to how to best improve each module! 🧵 
	  
	  ![](https://pbs.twimg.com/media/Fs9WS1WWwAIsQ3q.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1643627275236130816))
		- **Note**: Thread
	- The diagram 🖼️ above shows which components are stable and which are volatile.
	  
	  We’re actively working on making all interfaces well-defined.
	  
	  Meaning core stuff like indexes/query runner will be exposed soon 👀
	  
	  In the meantime, let’s take a look at the stable modules. ([View Tweet](https://twitter.com/jerryjliu0/status/1643627279229022208))
	- 📀Data Loaders: A data loader ingests data of any format from anywhere into Document objects, which can then be parsed and indexed.
	  
	  All found on https://t.co/HZYqDilLOP 🦙🏡
	  
	  Ideas 💡: Want to load something but there's no LlamaHub data loader for it yet? Make a PR! 
	  
	  ![](https://pbs.twimg.com/media/Fs9WTdUWYAoIm8o.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1643627286137020417))
	- 👓Node Parsers: A node parser parses Document objects into Node objects
	  
	  Example: https://t.co/QxqDdQkF2M
	  
	  Ideas 💡: Add new Node relationships to model to model hierarchical documents! 
	  
	  ![](https://pbs.twimg.com/media/Fs9WT3VWcAYKlzR.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1643627295289094144))
	- ✂️Text Splitters: Text splitter splits a long text string into smaller text string chunks.
	  
	  We have a naive default token splitter and a slightly better “sentence” splitter.
	  
	  Example: https://t.co/v7aZ9uYYso
	  
	  Ideas 💡: Come up with better text structuring/parsing techniques 
	  
	  ![](https://pbs.twimg.com/media/Fs9WUa0WIAEEib-.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1643627303715368971))
	- 🫙Vector Stores: Our vector store classes store embeddings and support lookup via similarity search.
	  
	  Example: https://t.co/EoH1JjR5cb
	  
	  Ideas 💡: See a vector db out there that we don’t support yet? Make a PR! 
	  
	  ![](https://pbs.twimg.com/media/Fs9WU_WWYAIYHel.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1643627313743921152))
	- 🦋Query Transforms: Our query transformations “change” a query given context to improve retrieval.
	  
	  There’s some really really cool stuff in here, from HyDE to our query decomposition work! 
	  
	  Guide: https://t.co/Nkp2qgESxx
	  
	  Ideas 💡: more transformations 💪 
	  
	  ![](https://pbs.twimg.com/media/Fs9WVkkWIAoaiBi.jpg) 
	  
	  ![](https://pbs.twimg.com/media/Fs9WVjhWwAIQOci.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1643627324313681921))
	- 🔮Optimizers: refines retrieved Nodes to reduce token usage for LLM’s (by up to 50%!) 
	  
	  Example nb: https://t.co/U1fJu2u5wc
	  
	  Ideas 💡: More token optimizers (extractive summarization techniques?) 
	  
	  ![](https://pbs.twimg.com/media/Fs9WWK9X0AAO1MU.jpg) 
	  
	  ![](https://pbs.twimg.com/media/Fs9WWK3WwAIhSoD.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1643627335134896135))
	- ⚙️Node Postprocessors: A node postprocessor refines a list of retrieved nodes.
	  
	  Can do super cool stuff like exploiting temporal links! https://t.co/7LuSBf56gV
	  
	  Ideas 💡: Sorting nodes by date, using the LLM to filter out Nodes, and more! 
	  
	  ![](https://pbs.twimg.com/media/Fs9WW3oWIAEW2Wz.jpg) 
	  
	  ![](https://pbs.twimg.com/media/Fs9WW3eWwAUeZac.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1643627347025723397))
	- 🛤️ Output Parsers AND Evaluation
	  
	  We’ve recently added initial evaluation modules and output parsing modules to LlamaIndex: https://t.co/cYPuNhonMt
	  
	  Ideas 💡: How do we best evaluate joint retrieval + LLM performance? 
	  
	  ![](https://pbs.twimg.com/media/Fs9WXj6WcAQMD9e.jpg) ([View Tweet](https://twitter.com/jerryjliu0/status/1643627359478636546))
	- Full details can be found in our contribution guide here: https://t.co/NPMjGWqsEa. 
	  
	  Huge shoutout to @disiok for putting this together. ([View Tweet](https://twitter.com/jerryjliu0/status/1643627364750880769))