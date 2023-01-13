title:: There's Been a Lot of Lo... (highlights)
author:: [[@MatthewJBar on Twitter]]
full-title:: "There's Been a Lot of Lo..."
category:: #tweets
url:: https://twitter.com/MatthewJBar/status/1605328892926885888

- Highlights first synced by [[Readwise]] [[Dec 21st, 2022]]
	- There's been a lot of low quality GPT-4 speculation recently. So, here's a relatively informed GPT-4 speculation thread from an outsider who still doesn't know that much. 🧵 ([View Tweet](https://twitter.com/MatthewJBar/status/1605328892926885888))
		- **Note**: Thread
	- In a blog post from 2020, Microsoft announced a new supercomputer for the exclusive purpose of training large ML models for OpenAI. They stated that "Compared with other machines listed on the TOP500 supercomputers in the world, it ranks in the top five".
	  
	  https://t.co/pm52MsRQgf ([View Tweet](https://twitter.com/MatthewJBar/status/1605328898383679488))
	- At the time, the top supercomputer listed by TOP500 was Summit from IBM, though the much faster Supercomputer Fugaku would be listed in the June 2020 TOP500 release one month later.
	  https://t.co/nuAV223RFc ([View Tweet](https://twitter.com/MatthewJBar/status/1605328901105803264))
	- The 1st and 5th supercomputers in the June 2020 release had a peak performance of 513.85 and 100.68 PFlop/s respectively, according to the LINPACK benchmark. However, the LINPACK benchmark uses FP64, which is much more precision than necessary for deep learning. ([View Tweet](https://twitter.com/MatthewJBar/status/1605328903567859714))
	- From NVIDIA, "The theoretical peak performance of the Tensor Cores on the V100 is approximately 120 TFLOPS. This is about an order of magnitude (10x) faster than double precision (FP64)"
	  https://t.co/3m0pbbIPyj ([View Tweet](https://twitter.com/MatthewJBar/status/1605328907074342912))
	- Given the last tweet, I naively estimate that the Microsoft supercomputer will attain a peak performance of somewhere between 4-10 times the FP64 performance of the 1st and 5th top supercomputers in the June TOP500 release. ([View Tweet](https://twitter.com/MatthewJBar/status/1605328909494468609))
	- This puts the peak performance of the Microsoft supercomputer in the range of 402.72 PFlop/s to 5138.5 PFlop/s. Of course, this figure refers only to peak performance. Utilization will likely be lower than 100%: I expect it to be somewhere around 40-80%. ([View Tweet](https://twitter.com/MatthewJBar/status/1605328912342343680))
	- We must also consider training time. This post from Epoch researchers predicts that training runs will likely not exceed ~1 year.
	  https://t.co/MFOEjO14Ka ([View Tweet](https://twitter.com/MatthewJBar/status/1605328914758266880))
	- My intuition also suggests that OpenAI will train GPT-4 for 6-12 months, given my understanding of the value of the project, and my knowledge of prior training runs. For example, their OpenAI Five model was trained over 296 days.
	  https://t.co/OCENyXmwyz ([View Tweet](https://twitter.com/MatthewJBar/status/1605328917510127616))
	- Combining these assumptions, I estimate that the total training compute for GPT-4 will be between 2.54 billion petaFLOP to 130 billion petaFLOP, with a central estimate of 18 billion petaFLOP. For comparison, that's roughly 1-50 times more compute than PaLM. 
	  
	  ![](https://pbs.twimg.com/media/FkcgiqjVQAAq6Zn.jpg) ([View Tweet](https://twitter.com/MatthewJBar/status/1605328925789278209))
	- The first Chinchilla scaling law predicts that a compute-optimal model trained with 130 petaFLOP will have a little over one trillion parameters, though the other scaling laws in the paper forecast something more in the range of 500 billion to 1 trillion. 
	  
	  ![](https://pbs.twimg.com/media/FkciRLTUUAAtxOY.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FkciSgpUoAAGBbW.jpg) ([View Tweet](https://twitter.com/MatthewJBar/status/1605328933188091904))
	- Given this information, I consider it unlikely that [[GPT-4]] will have more than one trillion parameters. And if it does, then I expect it will have just barely more than one trillion. Most likely, [[GPT-4]] will be comparable in size to [[GPT-3]], which had 175 billion parameters. ([View Tweet](https://twitter.com/MatthewJBar/status/1605328937453621249))
	- We can also assume that GPT-4 will be trained with fewer than 43.5 trillion tokens, possibly over multiple epochs due to data constraints. Of course, this is all assuming the Chinchilla scaling laws hold, which may not be a safe assumption. 
	  
	  ![](https://pbs.twimg.com/media/FkcjU0ZVEAM6jgc.jpg) ([View Tweet](https://twitter.com/MatthewJBar/status/1605328943162458112))
	- What qualitative performance should we expect from GPT-4? In my own opinion, a reasonable first-pass measure of qualitative performance is -log(KL divergence), which can be estimated using the parametric Chinchilla scaling law. ([View Tweet](https://twitter.com/MatthewJBar/status/1605328946656030721))
	- Using some publicly available data, and assuming each of these models are trained in a similar way Chinchilla was, we can compare the performance of [[GPT-4]] to [[GPT-2]], GPT-3, Chinchilla, and PaLM.
	  
	  (Note that the [[GPT-2]] calculation required major guesswork.) 
	  
	  ![](https://pbs.twimg.com/media/FkdCzW1UUAADpf3.jpg) ([View Tweet](https://twitter.com/MatthewJBar/status/1605328954012753920))
	- However, GPT-4 will probably include some algorithmic advances that Chinchilla lacks. The most salient possibility is that it will employ an explicit retrieval mechanism, similar to DeepMind's Retro model.
	  https://t.co/HYprGz61MT ([View Tweet](https://twitter.com/MatthewJBar/status/1605328957703716865))
	- From the paper, "Retro models gains do not diminish for models with up to at least 7B parameters, and correspond to non-retrieval models with 10× more parameters on certain datasets." ([View Tweet](https://twitter.com/MatthewJBar/status/1605328960383897600))
	- Let's calculate what GPT-4's performance would be if it used 10x more parameters without retrieval, and naively assume that will be its performance with retrieval. This is what we get. 
	  
	  ![](https://pbs.twimg.com/media/FkdC81dUUAEi2rX.jpg) ([View Tweet](https://twitter.com/MatthewJBar/status/1605328966197268480))
	- With the algorithmic adjustment, the qualitative improvement from [[GPT-3]] (vanilla) to [[GPT-4]] is comparable to the improvement from [[GPT-2]] to [[GPT-3]]. Since that was a rather big jump, I expect many will be stunned by GPT-4, especially those who expected strong diminishing returns. ([View Tweet](https://twitter.com/MatthewJBar/status/1605328969808547840))
	- However, there are many ways this analysis could be wrong. I have thus far assumed that Micosoft did not upgrade their supercomputer for OpenAI since 2020. In theory, I could be underestimating the training FLOP for GPT-4, and thus underestimating its performance. ([View Tweet](https://twitter.com/MatthewJBar/status/1605328972283199488))
	- Probably the most dubious assumption I made is that OpenAI will have enough high quality data to train their model compute-optimally. They've likely been working to scrape as much data from the internet as possible. But they may have hit a limit, e.g. see
	  https://t.co/wIHNOSmdgF ([View Tweet](https://twitter.com/MatthewJBar/status/1605328974850052096))
	- On the other hand @pvllss and others have estimated that we likely have a stock of high-quality language data on the internet exceeding 1e14 words, which is probably sufficient for now. However, not all of this data stock may be accessible to OpenAI.
	  https://t.co/pEhY2qdD8w 
	  
	  ![](https://pbs.twimg.com/media/FkdEwUzUEAEpmT0.jpg) ([View Tweet](https://twitter.com/MatthewJBar/status/1605328981133127680))
	- I may have also made some other mistakes in my calculations, assumptions, and plots. Regardless, I expect this rough conclusion to hold: assuming it's released, GPT-4 will be wild. ([View Tweet](https://twitter.com/MatthewJBar/status/1605328983968477184))
	- Correction: I probably slightly underestimated [[GPT-2]]'s performance in the plots. This makes the difference between [[GPT-2]] and [[GPT-3]] a bit smaller, and by consequence, makes the large predicted jump to GPT-4 look even more impressive. ([View Tweet](https://twitter.com/MatthewJBar/status/1605434648556736512))