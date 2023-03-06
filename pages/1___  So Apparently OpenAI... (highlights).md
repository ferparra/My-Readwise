title:: 1/  So Apparently OpenAI... (highlights)
author:: [[@Nicole_Janeway on Twitter]]
full-title:: "1/  So Apparently OpenAI..."
category:: #tweets
url:: https://twitter.com/Nicole_Janeway/status/1629656909417701378

- Highlights first synced by [[Readwise]] [[Feb 28th, 2023]]
	- 1/  So apparently OpenAI at one point trained and ran a model with sign-flipped reward due to a coding bug 🤦‍♀️
	  
	  "One of our code refactors introduced a bug which flipped the sign of the reward. Flipping the reward would usually produce incoherent text," ([View Tweet](https://twitter.com/Nicole_Janeway/status/1629656909417701378))
		- **Note**: Thread
	- 2/ "but the same bug also flipped the sign of the KL penalty. The result was a model which optimized for negative sentiment while preserving natural language. Since our instructions told humans to give very low ratings to continuations with sexually explicit text," ([View Tweet](https://twitter.com/Nicole_Janeway/status/1629656911338668032))
	- 3/  "the model quickly learned to output only content of this form. This bug was remarkable since the result was not gibberish but maximally bad output. The authors were asleep during the training process, so the problem was noticed only once training had finished." ([View Tweet](https://twitter.com/Nicole_Janeway/status/1629656912634736644))
	- 4/  "A mechanism such as Toyota’s Andon cord could have prevented this, by allowing any labeler to stop a problematic training process."
	  
	  from 
	  https://t.co/4oqwvPIBSp ([View Tweet](https://twitter.com/Nicole_Janeway/status/1629656914262134786))
	- 5/  Uh, can we get somebody on this, please?  Like, unit test best practices, or something? ([View Tweet](https://twitter.com/Nicole_Janeway/status/1629656916157931520))