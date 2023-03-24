title:: I Will Show You How to D... (highlights)
author:: [[@Iamrinders on Twitter]]
full-title:: "I Will Show You How to D..."
category:: #tweets
url:: https://twitter.com/Iamrinders/status/1637914960914259977

- Highlights first synced by [[Readwise]] [[Mar 24th, 2023]]
	- I will show you how to develop a chatbot using @LangChainAI library and @OpenAI ,  that:
	  
	  1- Retrieve the @zenml_io documentation
	  2- Answer to our questions, and gather related information. 
	  
	  Let's Dive in! ([View Tweet](https://twitter.com/Iamrinders/status/1637914960914259977))
		- **Note**: Thread
	- Step 1 - Install Langchain.
	  
	  We will use the @LangChainAI library to build a Large Language Model. 
	  
	  ![](https://pbs.twimg.com/media/FrsK_IJWIAAGZHp.jpg) ([View Tweet](https://twitter.com/Iamrinders/status/1637914972691808259))
	- Step 2 - Import OpenAI Library. 
	  
	  We will use the @OpenAI Embedding model. 
	  
	  ![](https://pbs.twimg.com/media/FrsK_1oWcAAPC5t.jpg) ([View Tweet](https://twitter.com/Iamrinders/status/1637914985543213057))
	- Step 3 - Store our unique API key. 
	  
	  ![](https://pbs.twimg.com/media/FrsLARtXoAUwUd0.jpg) ([View Tweet](https://twitter.com/Iamrinders/status/1637914992946077696))
	- Step 4 - Create a function to fetch all markdown files of ZenML's repository. 
	  
	  ![](https://pbs.twimg.com/media/FrsLBNFXgAAyGYG.jpg) ([View Tweet](https://twitter.com/Iamrinders/status/1637915009836613635))
	- The following actions are performed by the above process:
	- It scans through each markdown file (.md or .mdx) in the repository.
	- Step 5 - Use the above-created function to fetch md or mdx file data from the ZenML repository and store it in a variable. 
	  
	  ![](https://pbs.twimg.com/media/FrsLCcrX0AAhpst.jpg) ([View Tweet](https://twitter.com/Iamrinders/status/1637915029344247808))
	- Step 6 - Import CharacterTextSplitter. 
	  
	  It will break down our document text into small chunks and store them in a list. This will help in processing the text more efficiently 
	  
	  ![](https://pbs.twimg.com/media/FrsLERhWwAAKXhX.jpg) ([View Tweet](https://twitter.com/Iamrinders/status/1637915060709253122))
	- Step 7 - Import FAISS library and OpenAIEmbeddings 
	  
	  ![](https://pbs.twimg.com/media/FrsLEpqXwAAYQML.jpg) ([View Tweet](https://twitter.com/Iamrinders/status/1637915067751571458))
	- FAISS is a similarity search tool developed by Facebook AI. Its primary function is to allow for rapid searching of embeddings in multimedia documents that are similar to one another. ([View Tweet](https://twitter.com/Iamrinders/status/1637915070020694018))
	- In other words, it will search for text in transcriptions that closely match the text in our question or search.
	  
	  To use FAISS, the input data must be in the form of embeddings or vectors.
	  
	  Therefore, before feeding data to FAISS, the text must first be converted into embeddings. ([View Tweet](https://twitter.com/Iamrinders/status/1637915071954165762))
	- Once the text has been converted into embeddings, FAISS can compare and search for similar embeddings to those found in the question.
	  
	  To create embeddings, we will use a tool by OpenAI called OpenAIEmbeddings. ([View Tweet](https://twitter.com/Iamrinders/status/1637915073980116995))
	- Step 8 - Transform our text documents into vector form using FAISS and store it in a variable. 
	  
	  ![](https://pbs.twimg.com/media/FrsLFZ4WIAAypSv.jpg) ([View Tweet](https://twitter.com/Iamrinders/status/1637915080334426115))
	- Step 9 - Create a chain using ' load_qa_with_sources_chain ' tool
	  
	  ' load_qa_with_sources_chain ' will take in the query and lookup for the documents from the vector database (created by FAISS) of markdown files data, stored in variable stored. 
	  
	  ![](https://pbs.twimg.com/media/FrsLFx7X0AAkwky.jpg) ([View Tweet](https://twitter.com/Iamrinders/status/1637915087271784454))
	- Step 10 - Let's try our bot and ask it some questions. 
	  
	  ![](https://pbs.twimg.com/media/FrsLGO3WwAYRVeV.jpg) ([View Tweet](https://twitter.com/Iamrinders/status/1637915094947356677))
	- WOW! Our chatbot has correctly answered to all of our queries and furthermore, it has provided us with the appropriate source of information.
	  
	  Here is the colab notebook for the complete project:
	  
	  https://t.co/Q7aYdmG4Zp ([View Tweet](https://twitter.com/Iamrinders/status/1637915097887657987))
	- If you enjoyed this thread:
	  
	  1. Follow me  @Iamrinders for more of this content.
	  
	  2. RT the tweet below to share this thread with your audience https://t.co/aQAJshYEHM ([View Tweet](https://twitter.com/Iamrinders/status/1637915100307759105))