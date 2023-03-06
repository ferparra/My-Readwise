title:: @LangChainAI and #ChatGP... (highlights)
author:: [[@RLanceMartin on Twitter]]
full-title:: "@LangChainAI and \#ChatGP..."
category:: #tweets
url:: https://twitter.com/RLanceMartin/status/1631325764577816576

- Highlights first synced by [[Readwise]] [[Mar 6th, 2023]]
	- @LangChainAI and #ChatGPT API can be used to built a question-answer agents on top of local government regulations. Here I show ChatGPT working on top of San Francisco's building code as an example. https://t.co/cnVCFboYdy ([View Tweet](https://twitter.com/RLanceMartin/status/1631325764577816576))
		- **Note**: Thread
	- AI can act as a natural language interface between citizens and hard-to-parse rules / regulations. Building codes are one of the many areas this could be applied (@Noahpinion has written about this). https://t.co/nSBA4mT4fd ([View Tweet](https://twitter.com/RLanceMartin/status/1631325766414913536))
	- To avoid hallucination, I index the SF building code and store it (via @pinecone). #ChatGPT draws from the index to answer questions, acting just as a "brain" / distiller of the external information source. @LangChainAI wraps various endpoints to make this easy to implement. https://t.co/NWhvyKt1qp ([View Tweet](https://twitter.com/RLanceMartin/status/1631325768289779712))
	- More generally, we can think of the LLM as an agent that can answer questions about regulations, but also perform actions (e.g., fetch other documents or search) based on the context of the question. 
	  
	  ![](https://pbs.twimg.com/media/FqOaHUWagAA6x47.jpg) ([View Tweet](https://twitter.com/RLanceMartin/status/1631325772064636930))
	- E.g., I use @LangChainAI to create an agent and ask it to find the rules for a backyard shed (using our index of regulations) and then find sheds that meet these criteria (using Google). We can see the console output of the agent processing below. 
	  
	  ![](https://pbs.twimg.com/media/FqOacFdaMAAHnN-.jpg) ([View Tweet](https://twitter.com/RLanceMartin/status/1631325774421843970))
	- Kudos to @hwchase17 and team for integrating #chatGPT API and DBQA so quickly yesterday! I was able to code this last night (code linked in notion). https://t.co/6FB1mdY49K ([View Tweet](https://twitter.com/RLanceMartin/status/1631325777601110016))