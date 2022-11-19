title:: 📜🚨📜🚨 NN Loss Landscapes... (highlights)
author:: [[@SamuelAinsworth on Twitter]]
full-title:: "📜🚨📜🚨 NN Loss Landscapes..."
category:: #tweets
url:: https://twitter.com/SamuelAinsworth/status/1569719494645526529

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- 📜🚨📜🚨
	  NN loss landscapes are full of permutation symmetries, ie. swap any 2 units in a hidden layer. What does this mean for SGD? Is this practically useful?
	  
	  For the past 5 yrs these Qs have fascinated me. Today, I am ready to announce "Git Re-Basin"!
	  
	  https://t.co/mRu5k3ONUm https://t.co/vhrRSV2Cb7 ([View Tweet](https://twitter.com/SamuelAinsworth/status/1569719494645526529))
		- **Note**: Thread
	- We show that NN loss landscapes contain effectively only a single basin(!) provided sufficient width. Even better, we develop practical algos to navigate these basins... ([View Tweet](https://twitter.com/SamuelAinsworth/status/1569719497657057281))
	- Say you train Model A. 
	  
	  Independently, your friend trains Model B, possibly on different data. 
	  
	  With Git Re-Basin, you can merge models A+B in weight space at _no cost to the loss_ ([View Tweet](https://twitter.com/SamuelAinsworth/status/1569719499263471616))
	- Git Re-Basin applies to any NN arch & we provide the first-ever demonstration of zero-barrier linear mode connectivity between two independently trained (no pre-training!) ResNets.
	  
	  Put simply: a ResNet loss landscape contains only a single basin & we have algo to prove it ([View Tweet](https://twitter.com/SamuelAinsworth/status/1569719500966330375))
	- Phenomenon #1: "merge-ability" is an emergent property of SGD training -> merging at init doesn't work but a phase transition occurs such that it becomes possible over time 
	  
	  ![](https://pbs.twimg.com/media/Fchok19acAANxRp.jpg) 
	  
	  ![](https://pbs.twimg.com/media/Fchom7GaIAECc32.jpg) ([View Tweet](https://twitter.com/SamuelAinsworth/status/1569719506041450498))
	- Phenomenon #2: Model width is intimately related to merge-ability: the wider the better. Not too burdensome of a constraint since we're all training in the wide/overparameterized regime anyways. Important nonetheless... 
	  
	  ![](https://pbs.twimg.com/media/FchPJzKaQAAeMkc.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FchPLc1aIAIFma9.jpg) ([View Tweet](https://twitter.com/SamuelAinsworth/status/1569719511435341824))
	- Also, not all arch's are equally mergeable: VGGs seem to be harder than ResNets 🤷‍♂️ We hypothesize that merge-ability is an indicator of compatible data/arch fit. ([View Tweet](https://twitter.com/SamuelAinsworth/status/1569719514312626176))
	- Finally, my fav result: it's possible to train models on disjoint and biased datasets, then merge them together in weight space. 
	  
	  Eg, you have some data in US, some in EU. Can't mix data due to GDPR etc. Train separate models, merge weights -> generalize to the combined dataset! 
	  
	  ![](https://pbs.twimg.com/media/FchSDY1agAMIYrR.jpg) ([View Tweet](https://twitter.com/SamuelAinsworth/status/1569719518578221056))
	- So there ya go: it's possible to mix trained models like mixing potions, no pre-training or fine-tuning necessary. 
	  
	  That said, there are still loads of open questions left! I'm v curious to see where LMC and model patching work goes in the future 🚀 ([View Tweet](https://twitter.com/SamuelAinsworth/status/1569719520759250944))
	- Also plenty of exciting possible applications to federated learning, distributed training, deep learning optimization, and so forth ([View Tweet](https://twitter.com/SamuelAinsworth/status/1569719522109816832))
	- Ok, that's enough for one thread... Check out algos, counterexamples, proofs, and more in 
	  
	  the paper (https://t.co/mRu5k3ONUm) 
	  and code (https://t.co/kF6PscpkNr) ([View Tweet](https://twitter.com/SamuelAinsworth/status/1569719523447832576))
	- Joint work with Jonathan Hayase and @siddhss5. Inspired by work from @colinraffel, @rahiment, @jefrankle, @RAIVNLab folks, and many other beautiful people!
	  
	  Shout out to @Mitchnw, @adityakusupati, @RamanujanVivek and others who came along the ride! ([View Tweet](https://twitter.com/SamuelAinsworth/status/1569719525029089283))
	- Oh I forgot to add: our weight matching algo (sec 3.2) runs in ~10 seconds. So you won't be waiting around all day! ([View Tweet](https://twitter.com/SamuelAinsworth/status/1569765714868977664))