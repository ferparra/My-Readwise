title:: I've Never Had So Many "... (highlights)
author:: [[@ch402 on Twitter]]
full-title:: "I've Never Had So Many "..."
category:: #tweets
url:: https://twitter.com/ch402/status/1570096782390226944

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- I've never had so many "this can't possibly be true, we must have a bug" results in the course of a research project before.
	  
	  I'd like to take a moment to walk through some of the very strange (and surprisingly beautiful) things we found. https://t.co/wZnLe61Z2I ([View Tweet](https://twitter.com/ch402/status/1570096782390226944))
		- **Note**: Thread
	- Firstly: Superposition by itself is utterly wild if you take it seriously. 
	  
	  It's basically saying that neural networks might be bigger -- potentially *much* bigger -- than their surface structure implies, simulating a larger sparser system. ([View Tweet](https://twitter.com/ch402/status/1570096783891603461))
	- Let's warm up with a mildly surprising fact: Superposition is a *phase* separated by a discontinuous change in importance-sparsity space.
	  
	  It's also a *per-feature phase change* rather than model level phase change. https://t.co/31ZFj9aI65 ([View Tweet](https://twitter.com/ch402/status/1570096785120436229))
	- OK, I can buy that. But... oh dear.
	  
	  Why is there a *tetrahedron* in my neural net??? 
	  
	  What is going on??? https://t.co/6ywVeCYsO6 ([View Tweet](https://twitter.com/ch402/status/1570096787276300289))
	- That's just the start.  As models train, there's this discrete "energy level jump" like behavior, associated with sharp drops in loss. 🤯
	  
	  Uh, well, maybe that suggest a hypothesis for grokking at least?? Even if it makes me very confused. 
	  
	  ![](https://pbs.twimg.com/media/FcoWkCqXoAMg2EX.jpg) ([View Tweet](https://twitter.com/ch402/status/1570096791520952320))
	- In other regimes, the learning dynamics of our models are governed by simple geometric transformations. Each corresponding to bumps in the loss curve. ✨ 
	  
	  ![](https://pbs.twimg.com/media/FcoW36rWYAMa9yM.jpg) ([View Tweet](https://twitter.com/ch402/status/1570096796600512513))
	- Ok, superposition is weird...
	  
	  But why is it extremely correlated with vulnerability to adversarial examples (at least in our toy models)? Like, very correlated.
	  
	  (OK, at least there are hypotheses about this.) 
	  
	  ![](https://pbs.twimg.com/media/FcoXbhcXEAAa9j8.jpg) ([View Tweet](https://twitter.com/ch402/status/1570096803793588224))
	- This part is a little less surprising: if you add an activation to the hidden layer, the features start to align with neurons.
	  
	  Finally something that makes me less confused. This starts to offer an explanation for "monosemantic" and "polysemantic" neurons and why we see both. 
	  
	  ![](https://pbs.twimg.com/media/FcoXsH0XEAMq_xw.jpg) ([View Tweet](https://twitter.com/ch402/status/1570096809896443910))
	- But there are hints that there's some kind of "neuron level phase change" going on which causes neurons to switch between being monosemantic and polysemantic!! 
	  
	  ![](https://pbs.twimg.com/media/FcoYP4LXkAILKaX.jpg) ([View Tweet](https://twitter.com/ch402/status/1570096815499796480))
	- Also... it's not just that neural networks can store extra features in superposition. They can *do computation* while they're in superposition!! So in some sense, they can actually simulate a more complex (but very sparse) computational structure. ([View Tweet](https://twitter.com/ch402/status/1570096818624528392))
	- There's a lot more in the paper, but I think those are some of the weirdest things for me. 
	  
	  Keep in mind that there's a big caveat: we've only shown this for small ReLU networks trained on synthetic data. Who knows to what extent this reflects real neural nets. ([View Tweet](https://twitter.com/ch402/status/1570096820533207040))
	- (Although I'd personally now feel quite comfortable betting that the high-level superposition hypothesis is true, at leas to some extent.) ([View Tweet](https://twitter.com/ch402/status/1570096821908684806))
	- BTW, a huge shout out to all our colleagues, both at Anthropic and other orgs. So many people generously made time to help us. ([View Tweet](https://twitter.com/ch402/status/1570096823334850560))
	- Especially grateful to Kshitij Sachan, @banburismus_, Jeff Wu, and Dan Mossing who *did independent replications* https://t.co/ZBAvMFXL18 
	  
	  ![](https://pbs.twimg.com/media/FcoZlOvXoAE8ELR.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FcoZtKfXwAIpj2S.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FcoZvicWQAIiFW3.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FcoZxNVXkAECFBO.jpg) ([View Tweet](https://twitter.com/ch402/status/1570096828091179010))