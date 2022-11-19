title:: GPT-3 Is Amazing at Comp... (highlights)
author:: [[@npew on Twitter]]
full-title:: "GPT-3 Is Amazing at Comp..."
category:: #tweets
url:: https://twitter.com/npew/status/1525900849888866307

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- GPT-3 is amazing at complex tasks like creative writing and summarizing. But it's surprisingly bad at reversing words. 🤔
	  
	  The reason is that GPT-3 doesn't see the world the way we humans do. 👀
	  
	  If you teach it to reason, it can get around its limitations to get really good. 💡 
	  
	  ![](https://pbs.twimg.com/media/FS0SeqKVIAAA5us.jpg) ([View Tweet](https://twitter.com/npew/status/1525900849888866307))
		- **Note**: Thread
	- The first reason GPT-3 is bad at reversing words is due to tokenization: it doesn't see letters and words as humans do. Instead, it sees "tokens." ([View Tweet](https://twitter.com/npew/status/1525900851956420608))
	- Tokens are chunks of characters. For example, the word “alphabet” gets broken up into the tokens “alph" and "abet”. Short and common words like “the” are a single token. ([View Tweet](https://twitter.com/npew/status/1525900853189586944))
	- We can make GPT-3 "see" the letters by having it add spaces between them. Then each letter becomes its own token: " a", " l", " p" and so on. 
	  
	  ![](https://pbs.twimg.com/media/FS0SubRVIAAu4K5.jpg) ([View Tweet](https://twitter.com/npew/status/1525900856024920064))
	- But it's still not great at reversing words, because it gets "confused" by the ordering in long sequences.
	  
	  This is the second reason GPT-3 is bad at reversing words. 
	  
	  ![](https://pbs.twimg.com/media/FS0S1GOUsAYffno.jpg) ([View Tweet](https://twitter.com/npew/status/1525900859464241152))
	- We can teach it to order characters by having it add numbers to keep track of the letters in the sequence.
	  
	  This simple trick makes the ordering explicit, and GPT-3 now manages to reverse the letters correctly. 
	  
	  ![](https://pbs.twimg.com/media/FS0TOVPUAAEWm0M.jpg) ([View Tweet](https://twitter.com/npew/status/1525900863100702721))
	- So close! It manages to reverse the letter sequence, but fails at removing the spaces in the last step. It's the tokenization striking again. ([View Tweet](https://twitter.com/npew/status/1525900864644186112))
	- GPT-3 has trouble removing the spaces and merging tokens.
	  
	  You can teach it to break down the task into steps. In each step, you remove every other space: "a l p h a b e t" becomes "al ph ab et", which becomes "alph abet", and finally "alphabet". ([View Tweet](https://twitter.com/npew/status/1525900865596297216))
	- And that's it!  🎉 GPT-3 correctly reverses long words! But to get there, we had to teach GPT-3 the algorithm to use to get around its limitations. 💪 
	  
	  ![](https://pbs.twimg.com/media/FS0Tty2UAAAvr4U.jpg) ([View Tweet](https://twitter.com/npew/status/1525900868305833984))
	- Compare this to humans: We learn similar techniques to get around our limitations. 👨🏻‍🎓
	  
	  I'm pretty bad at adding large numbers. But I can do it with pen and paper. By writing it out, and reasoning through the steps, I can get around the limitations of my brain. 
	  
	  ![](https://pbs.twimg.com/media/FS0T6wQUUAA1jgB.jpg) ([View Tweet](https://twitter.com/npew/status/1525900871086665734))
	- It turns out that a similar approach can be used to teach GPT-3 to solve grade school math problems: https://t.co/kuWe6Bodch ([View Tweet](https://twitter.com/npew/status/1525900872344928256))
	- The takeaway here is that large language models like GPT-3 might be smarter than we think.
	  
	  You wouldn't expect humans to solve hard problems without breaking them down and reasoning through the steps.
	  
	  We're just getting started at seeing what these models are capable of. ✨ ([View Tweet](https://twitter.com/npew/status/1525900873334812672))
	- Try out GPT-3 for yourself in the OpenAI API: https://t.co/meVOHx3BeG ([View Tweet](https://twitter.com/npew/status/1525900874425372672))