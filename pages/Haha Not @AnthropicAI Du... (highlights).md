title:: Haha Not @AnthropicAI Du... (highlights)
author:: [[@altryne on Twitter]]
full-title:: "Haha Not @AnthropicAI Du..."
category:: #tweets
url:: https://twitter.com/altryne/status/1656707132195209216

- Highlights first synced by [[Readwise]] [[May 15th, 2023]]
	- haha not @AnthropicAI dumping the WHOLE @LangChainAI documentation in 1 prompt to ask for a summary! 
	  
	  Huge context windows are going to change the game so much! 
	  
	  Bye bye all the "chat with PDF" startups I guess ([View Tweet](https://twitter.com/altryne/status/1656707132195209216))
		- **Note**: Thread
	- @AnthropicAI @LangChainAI Apparently available via API (I couldn't find it in the UI! how do I upload documents @AnthropicAI ??) 
	  
	  There are now several, 100K versions of their models! 
	  
	  ![](https://pbs.twimg.com/media/Fv3aKruaQAUl4ri.jpg) ([View Tweet](https://twitter.com/altryne/status/1656720209322070018))
	- @AnthropicAI @LangChainAI I am trying to paste my whole tweet archive history in YAML format directly into @AnthropicAI Claude playground, the browser is frozen 🫣 
	  
	  ![](https://pbs.twimg.com/media/Fv3lggUagAEYl1Y.jpg) ([View Tweet](https://twitter.com/altryne/status/1656732600868966400))
	- Haha ok I was able to run a few of my tweet (apparently I tweet a LOT! 1 year of tweets is way above 100K tokens for me 😅 Needed to extract a sample) 
	  
	  Here I am providing @AnthropicAI with 98889 tokens of tweets in yaml format with dates etc and asking for a summary: 
	  
	  Here's… 
	  
	  ![](https://pbs.twimg.com/media/Fv4hWo-aQAAI32T.jpg) ([View Tweet](https://twitter.com/altryne/status/1656798898487463940))
	- BTW it took only 38 seconds to part 100K tokens and return a summary 🤯 ([View Tweet](https://twitter.com/altryne/status/1656799413359239168))
	- Interestingly, the total tokens allowed are MORE than 100K haha 
	  
	  ![](https://pbs.twimg.com/media/Fv4lTMOaYAA1JrH.jpg) ([View Tweet](https://twitter.com/altryne/status/1656802767858724864))
	- So the "claude-instant-100k" model took 38 seconds, the claude-v1.3-100k model took 2 minutes and it's way way better at summarization! 
	  
	  However, I cannot seem to get Claude to ... get me the top most tweets. It's always doing a summary. ([View Tweet](https://twitter.com/altryne/status/1656805007520595968))
	- Yes! I knew it, the langchain docs don't seem to jazz with how @AnthropicAI wants things. (cc @hwchase17 ) 
	  
	  The SystemMessage seemed to have 0 effect, and I followed the examples from Anthropic documentation and shoved the system message AND the user one and it worked! 
	  
	  ![](https://pbs.twimg.com/media/Fv4pb1JakAA5-Zs.jpg) ([View Tweet](https://twitter.com/altryne/status/1656807365126270976))
	- The more competent Claude v1.3 model is definitely more competent. However, bigger context does NOT mean, 0 hallucinations. 
	  
	  I asked it to return the top (by likes and retweets) tweets and return each one with a link. It did the links correctly, but many of them are just...… 
	  
	  ![](https://pbs.twimg.com/media/Fv4qKvGaMAEOTRP.jpg) ([View Tweet](https://twitter.com/altryne/status/1656808407394033664))
	- How can we trust a model that confabulates numbers? 
	  
	  https://t.co/N9LCxYGzaE ([View Tweet](https://twitter.com/altryne/status/1656813457302523904))
	- It's VERY interesting. 
	  
	  Claude is indeed able to figure out what are some of the top tweets are, but not all of them, it obviously omitted a few. 
	  
	  Then for the ones it did find, it confabulates a few of the details. Text seems to be 100% exact but numbers are off. ([View Tweet](https://twitter.com/altryne/status/1656816375191715840))
	- Another tidbit, per logs it seems that Antropic falls back to the regular model if you pass less than 9K tokens. 
	  I haven't changed the code for model selection, just the amount of tweets and logs show claude v1.3 vs v1.3-100K 
	  
	  ![](https://pbs.twimg.com/media/Fv43B03aIAARESH.jpg) ([View Tweet](https://twitter.com/altryne/status/1656822399894179840))
	- Very interestingly, Claude V1.3 with 9K tokens, does NOT confabulate on the same task. 
	  
	  Sorts the tweets properly by combined like+favorite, and all IDs are right! 
	  
	  So I gotta wonder if this is the result of some tricks they are doing with 100K 
	  
	  @karinanguyen_ any idea why? ([View Tweet](https://twitter.com/altryne/status/1656830041597296640))