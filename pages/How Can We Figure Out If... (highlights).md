title:: How Can We Figure Out If... (highlights)
author:: [[@CollinBurns4 on Twitter]]
full-title:: "How Can We Figure Out If..."
category:: #tweets
url:: https://twitter.com/CollinBurns4/status/1600892261633785856

- Highlights first synced by [[Readwise]] [[Jan 17th, 2023]]
	- How can we figure out if what a language model says is true, even when human evaluators can’t easily tell?
	  
	  We show (https://t.co/cBapz1OGzo) that we can identify whether text is true or false directly from a model’s *unlabeled activations*. 🧵 ([View Tweet](https://twitter.com/CollinBurns4/status/1600892261633785856))
		- **Note**: Thread
	- Existing techniques for training language models are misaligned with the truth: if we train models to imitate human data, they can output human-like errors; if we train them to generate highly-rated text, they can output errors that human evaluators can’t assess or don’t notice. ([View Tweet](https://twitter.com/CollinBurns4/status/1600892263412162563))
	- We propose trying to circumvent this issue by directly finding latent “truth-like” features inside language model activations without using any human supervision in the first place. ([View Tweet](https://twitter.com/CollinBurns4/status/1600892265094053888))
	- Informally, instead of trying to explicitly, externally specify ground truth labels, we search for implicit, internal “beliefs” or “knowledge” learned by a model. ([View Tweet](https://twitter.com/CollinBurns4/status/1600892267719716865))
	- This may be possible to do because truth satisfies special structure: unlike most features in a model, it is *logically consistent* ([View Tweet](https://twitter.com/CollinBurns4/status/1600892269363875840))
	- We make this intuition concrete by introducing Contrast-Consistent Search (CCS), a method that searches for a direction in activation space that satisfies negation consistency. 
	  
	  ![](https://pbs.twimg.com/media/Fjd-A8RacAArxji.jpg) ([View Tweet](https://twitter.com/CollinBurns4/status/1600892274980061189))
	- We find that on a diverse set of tasks (NLI, sentiment classification, cloze tasks, etc.), our method can recover correct answers from model activations with high accuracy (even outperforming zero-shot prompting) despite not using any labels or model outputs. ([View Tweet](https://twitter.com/CollinBurns4/status/1600892277723115521))
	- Among other findings, we also show that CCS really recovers something different from just the model outputs; it continues to work well in several cases where model outputs are unreliable or uninformative. ([View Tweet](https://twitter.com/CollinBurns4/status/1600892279472164864))
	- Of course, our work has important limitations and creates many new questions for future work. CCS still fails sometimes and there’s still a lot that we don’t understand about when this type of approach should be feasible in the first place. ([View Tweet](https://twitter.com/CollinBurns4/status/1600892281187618816))
	- Nevertheless, we found it surprising that we could make substantial progress on this problem at all.
	  
	  (Imagine recording a person's brain activity as you tell them T/F statements, then classifying those statements as true or false just from the raw, unlabeled neural recordings!) ([View Tweet](https://twitter.com/CollinBurns4/status/1600892283053690880))
	- This problem is important because as language models become more capable, they may output false text in increasingly severe and difficult-to-detect ways. Some models may even have incentives to deliberately “lie”, which could make human feedback particularly unreliable. ([View Tweet](https://twitter.com/CollinBurns4/status/1600892284702429185))
	- However, our results suggest that unsupervised approaches to making models truthful may also be a viable – and more scalable – alternative to human feedback.
	  
	  For many more details, please check out our paper (https://t.co/cBapz1OGzo) and code (https://t.co/hJaUk6ntqZ)! ([View Tweet](https://twitter.com/CollinBurns4/status/1600892286254346242))
	- (And a huge thanks to my excellent collaborators -- Haotian Ye, Dan Klein, and @JacobSteinhardt -- for helping make this happen!) ([View Tweet](https://twitter.com/CollinBurns4/status/1600892288020148224))