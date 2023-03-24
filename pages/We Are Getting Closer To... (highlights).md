title:: We Are Getting Closer To... (highlights)
author:: [[@justLV on Twitter]]
full-title:: "We Are Getting Closer To..."
category:: #tweets
url:: https://twitter.com/justLV/status/1637876167763202053

- Highlights first synced by [[Readwise]] [[Mar 21st, 2023]]
	- We are getting closer to “Her” (part 2!)
	  
	  Conversationally do anything with emails, using LLM chaining & few-shot prompting for tool use (@LangChainAI inspired)
	  
	  This is now realtime (ish), thanks to #OpenAI gpt-3.5-turbo
	  
	  🔈 on for voice realism! 
	  
	  🧵 https://t.co/svON91eEFu ([View Tweet](https://twitter.com/justLV/status/1637876167763202053))
		- **Note**: Thread
	- @LangChainAI This provides an incredibly natural way of searching for emails & then referencing them
	  
	  “are there any unread emails mentioning X in the last month?”
	  
	  “tell me more about the last one”
	  
	  “who else was cc’d on the picnic one?”
	  
	  “reply to the one about X saying …”
	  
	  another e.g.: https://t.co/4hXzKo1YCa ([View Tweet](https://twitter.com/justLV/status/1637877992067321856))
	- Native iOS integration was done through Shortcuts, see this thread for how I did this previously https://t.co/wbkCIk8alL ([View Tweet](https://twitter.com/justLV/status/1637881366011584513))
	- I originally manually chained responses, keeping track of and pruning history to feed into the next chain, and using stop tokens to prevent the LLM from hallucinating the API response.
	  
	  There was some refactoring & experimentation to make use of the new chat completions API... ([View Tweet](https://twitter.com/justLV/status/1637881367265701889))
	- What worked best for me was putting the prompt and few-shot examples in the “system” message, and getting the assistant to think it is providing the command to the user, who will then query the API and return results to the assistant to summarize (see e.g.) 
	  
	  ![](https://pbs.twimg.com/media/FrrrqKDaYAAdsYb.png) ([View Tweet](https://twitter.com/justLV/status/1637881368381382656))
	- 3 email commands are learned (which are then formatted into a GMail API request):
	- It is pretty surreal seeing e-mail replies coming in before the voice response is generated. 
	  
	  ![](https://pbs.twimg.com/media/FrrsyZxaMAI_DiP.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FrrsyZ2aUAAs-2Q.jpg) ([View Tweet](https://twitter.com/justLV/status/1637883357517475842))
	- It’s an incredible time to be building interactive experiences.
	  
	  (Unposted) voice experiments I've been running are  smart home control from Pi's, a morning chat briefed with my daily priorities, events, weather, sleep data etc.
	  
	  See my profile for other creative AI experiments ([View Tweet](https://twitter.com/justLV/status/1637883358800928770))