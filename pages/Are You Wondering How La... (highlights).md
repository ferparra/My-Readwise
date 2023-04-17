title:: Are You Wondering How La... (highlights)
author:: [[@iScienceLuvr on Twitter]]
full-title:: "Are You Wondering How La..."
category:: #tweets
url:: https://twitter.com/iScienceLuvr/status/1608070009921900546

- Highlights first synced by [[Readwise]] [[Apr 13th, 2023]]
	- Are you wondering how large language models like ChatGPT and InstructGPT actually work?
	  
	  One of the secret ingredients is RLHF - Reinforcement Learning from Human Feedback.
	  
	  Let's dive into how RLHF works in 8 tweets! ([View Tweet](https://twitter.com/iScienceLuvr/status/1608070009921900546))
		- **Note**: Thread
	- Large language models (LLMs) are trained w/ self-supervised learning using next token prediction which actually makes it bad for instruction following. This example from OpenAI's blog exemplifies how GPT-3 succeeds at next-token prediction but fails at instruction-following. 1/8 
	  
	  ![](https://pbs.twimg.com/media/FlEDKBRaEAEWBWA.png) ([View Tweet](https://twitter.com/iScienceLuvr/status/1608070017488408577))
	- What if we could use human-annotated data to improve our language model? One approach, known as supervised fine-tuning (SFT), is to take your pretrained LLM and fine-tune it with (prompt, human-written response) pairs. 2/8 
	  
	  ![](https://pbs.twimg.com/media/FlEDKbeaAAAC7dq.png) ([View Tweet](https://twitter.com/iScienceLuvr/status/1608070024950067200))
	- While SFT and related methods can perform quite well (the original InstructGPT models were just SFT/related models!), human annotation is quite expensive and hard to obtain. RLHF tries to alleviate some of that human annotation cost using what is known as a reward model. 3/8 ([View Tweet](https://twitter.com/iScienceLuvr/status/1608070028091625474))
	- We start with an LLM (can be the SFT one, which is what OpenAI does) & ask it to generate multiple responses for a prompt. Then a human ranks the responses. We then train the reward model to learn how the human would rank the responses and give a "reward" score per response. 4/8 
	  
	  ![](https://pbs.twimg.com/media/FlEDLCvagAA-tLG.jpg) ([View Tweet](https://twitter.com/iScienceLuvr/status/1608070037721735168))
	- Now that we have encapsulated our human feedback into this reward model, we use RL to fine-tune the language model.
	  
	  A common RL algorithm is proximal policy optimization (PPO). To apply PPO to fine-tuning language models, we start with an initial LM & a copy for fine-tuning. 5/8 ([View Tweet](https://twitter.com/iScienceLuvr/status/1608070041798574081))
	- We give both models a prompt and get a response. We score the tuned LLM response with our reward model. We try to update the parameters of our fine-tuned LLM to maximize our reward model score. 6/8 
	  
	  ![](https://pbs.twimg.com/media/FlEDL0naEAA_tdi.jpg) ([View Tweet](https://twitter.com/iScienceLuvr/status/1608070050866659331))
	- But we also don't want it to deviate too much from the initial response, which is what the KL penalty is used for. Otherwise the optimization might result in an LLM that produces gibberish but maximizes the reward model score. 7/8 ([View Tweet](https://twitter.com/iScienceLuvr/status/1608070054352130048))
	- It's that simple! This approach results in much better completions! Quantitative human evaluations indicate it's better than regular GPT, prompt-engineered GPT, and even SFT-trained GPT! 8/8 
	  
	  ![](https://pbs.twimg.com/media/FlEDMiEakAAaxC2.png) 
	  
	  ![](https://pbs.twimg.com/media/FlEDMv4aYAAeINu.jpg) ([View Tweet](https://twitter.com/iScienceLuvr/status/1608070064871469058))
	- If you are interested in exploring RLHF, check out open-source tools like TRLX, a library @carperai has created (which they will be using to train their OpenInstruct model)
	  
	  Link → https://t.co/To3dZp55vm
	  
	  I wrote an example walk-thru thread:
	  https://t.co/n2eYn1ufDs ([View Tweet](https://twitter.com/iScienceLuvr/status/1608070068117860352))
	- Here are some more in-depth resources (figures were taken from here):
	  @OpenAI blog post - https://t.co/JIHtpBc6rc
	  
	  @carperai & @huggingface blog post - https://t.co/BCl8CaByxa
	  
	  InstructGPT paper - https://t.co/2VXhz0kK1o ([View Tweet](https://twitter.com/iScienceLuvr/status/1608070071062265858))
	- If you liked this thread, consider sharing this thread 🙏
	  
	  and follow me for more ML content! 🙂 → @iScienceLuvr ([View Tweet](https://twitter.com/iScienceLuvr/status/1608070073885024257))