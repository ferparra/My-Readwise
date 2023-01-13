title:: // Algorithm Distillatio... (highlights)
author:: [[@ai__pub on Twitter]]
full-title:: "// Algorithm Distillatio..."
category:: #tweets
url:: https://twitter.com/ai__pub/status/1611786033653493760

- Highlights first synced by [[Readwise]] [[Jan 8th, 2023]]
	- // Algorithm Distillation, Explained //
	  
	  Using Algorithm Distillation (AD), DeepMind scientists trained transformers to "learn how to learn":
		- **Note**: Thread
	- TL;DR: A team from DeepMind trained transformers to:
	- How does AD differ from Gato, or Decision Transformers -  single models that can act in a wide variety of RL environments?
	  
	  These methods learn fixed RL policies - not the actual learning algorithms that improve policies as they encounter new data.
	  
	  AD can learn in-context.
	  
	  3/17 
	  
	  ![](https://pbs.twimg.com/media/Fl425F-akAEDrvG.jpg) ([View Tweet](https://twitter.com/ai__pub/status/1611786079388196867))
	- Think of a policy as a fixed set of actions given a sequence of observations. In contrast, RL algorithms have the ability to dynamically learn policies in any environment.
	  
	  Now, how does AD work? Let's get into the data, loss, and context used to train the transformer:
	  
	  4/17 ([View Tweet](https://twitter.com/ai__pub/status/1611786083787997184))
	- First, the architecture:
	  
	  The authors train AD using the GPT architecture.
	  
	  But AD is compatible with any sequence model such as RNNs, GRUs, LSTMs, etc.
	  
	  However, causal transformers are the most effective.
	  
	  5/17 
	  
	  ![](https://pbs.twimg.com/media/Fl4258lakAAjESP.jpg) ([View Tweet](https://twitter.com/ai__pub/status/1611786097239162881))
	- Second, the data.
	  
	  A large dataset is generated from the training histories of an RL algorithm across many different tasks.
	  
	  Each history is a collection of observations (states), actions, and rewards across multiple time-steps.
	  
	  6/17 
	  
	  ![](https://pbs.twimg.com/media/Fl426zLaAAcuKkN.jpg) 
	  
	  ![](https://pbs.twimg.com/media/Fl427LIaYAEyU_g.jpg) ([View Tweet](https://twitter.com/ai__pub/status/1611786113424953344))
	- Third, the model and loss.
	  
	  A transformer is used to "model actions causally, using the preceding learning history as context."
	  
	  A log-likelihood loss is used to (pre)-train the model.
	  
	  All the training is done based on predicting the actions. No Q values required!
	  
	  7/17 
	  
	  ![](https://pbs.twimg.com/media/Fl427tdaYAAhL01.jpg) ([View Tweet](https://twitter.com/ai__pub/status/1611786121696145408))
	- Note that this is pre-training. After pre-training, the AD model weights are frozen, and no fine-tuning is performed.
	  
	  Yet the model is still able to learn new RL algorithms in-context!
	  
	  8/17 ([View Tweet](https://twitter.com/ai__pub/status/1611786125240340482))
	- Finally, the context: the key to making AD work.
	  
	  Transformers are built to attend to context. However, previous works didn't utilize a long enough context.
	  
	  By including multi-episodic contexts in the training data, AD actually learns an operator for policy improvement.
	  
	  9/17 
	  
	  ![](https://pbs.twimg.com/media/Fl428VJaAAIsa8Q.jpg) ([View Tweet](https://twitter.com/ai__pub/status/1611786134102880257))
	- They show that AD can effectively distill any RL algorithm, including UCB, DQN, and A3C.
	  
	  They test on environments that cannot be solved via zero-shot generalization after pre-training:
	- AD matches the asymptotic RL performance on the dark room environments and comes close to it on Watermaze.
	  
	  How long must the context be to achieve this level of performance?
	  
	  They find that multi-episodic contexts of 2-4 episodes are needed.
	  
	  11/17 
	  
	  ![](https://pbs.twimg.com/media/Fl429rdacAACzfS.jpg) ([View Tweet](https://twitter.com/ai__pub/status/1611786158840909824))
	- They also find that AD is more data efficient than certain RL algorithms.
	  
	  Specifically, A3C and DQN run multiple actors in parallel in order to achieve good performance. AD is able to attain the same performance using only a single-stream version.
	  
	  12/17 
	  
	  ![](https://pbs.twimg.com/media/Fl42-alaAAEANGP.jpg) ([View Tweet](https://twitter.com/ai__pub/status/1611786170941468672))
	- What does Algorithm Distillation mean for RL?
	  
	  First, it showcases the power of transformer methods.
	  
	  When given enough context, they are able not only to learn specific policies, but also the complex RL algorithms that give rise to those policies!
	  
	  13/17 ([View Tweet](https://twitter.com/ai__pub/status/1611786175009943554))
	- Second, RL algorithms are notorious for data inefficiency.
	  
	  The fact that AD is drastically more data efficient means that RL algorithms will now be more accessible to those with less compute at their disposal - and more powerful given fixed data.
	  
	  14/17 ([View Tweet](https://twitter.com/ai__pub/status/1611786177698484227))
	- That's a wrap on Algorithm Distillation! You now understand, at a high level:
	- To learn more about Algorithm Distillation, see the original paper here: https://t.co/WcR8XyrQyd
	  
	  Also check out this thread by @MIshaLaskin, one of the scientists behind Algorithm Distillation!
	  
	  16/17 https://t.co/8JvcQhttj8 ([View Tweet](https://twitter.com/ai__pub/status/1611786183109120000))
	- AI Pub runs a talent network for senior software engineers, ML engineers, and ML scientists looking for their next role at cutting-edge AI startups.
	  
	  If that sounds like you, fill out this form and we'll be in touch! https://t.co/dPKkeI3lvF
	  
	  17/17 ([View Tweet](https://twitter.com/ai__pub/status/1611786186158411776))