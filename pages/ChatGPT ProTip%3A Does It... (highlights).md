title:: ChatGPT ProTip: Does It... (highlights)
author:: [[@alexandrosM on Twitter]]
full-title:: "ChatGPT ProTip: Does It..."
category:: #tweets
url:: https://twitter.com/alexandrosM/status/1649461937410031616

- Highlights first synced by [[Readwise]] [[Apr 22nd, 2023]]
	- ChatGPT ProTip:
	  
	  Does it annoy you when ChatGPT stops printing code in the middle of a file, you ask it to continue, and it starts printing without highlighting?
	  
	  Here's the easiest way to get it to continue the codeblock:
	  
	  ```
	  Continue
	  
	  (Read on for why I think this works) 
	  
	  ![](https://pbs.twimg.com/media/FuQQ5BDaEAA8bHJ.jpg) ([View Tweet](https://twitter.com/alexandrosM/status/1649461937410031616))
		- **Note**: Thread
	- What I think is happening is that it is not aware of how its output is being rendered, and there is some markdown to html layer in the ui that converts the interrupted markdown to the codeblock. ([View Tweet](https://twitter.com/alexandrosM/status/1649463211786399749))
	- So when you ask it to continue, as far as it knows, it is still in the markdown code block, which is why it doesn't think it should restart it. ([View Tweet](https://twitter.com/alexandrosM/status/1649463281286000640))
	- By closing the markdown codeblock it in my response, I'm showing it that the code block has been closed, and it infers it should start a new one before continuing with the code. ([View Tweet](https://twitter.com/alexandrosM/status/1649463304228855814))
	- Another observation that is explained by the hypothesis above:
	  
	  https://t.co/dwD2w5aLS9 ([View Tweet](https://twitter.com/alexandrosM/status/1649477799043039233))