title:: // Algorithm Distillation, Explained // (highlights)
author:: [[AI Pub]]
full-title:: "// Algorithm Distillation, Explained //"
category:: #articles
url:: https://twitter.com/ai__pub/status/1611786033653493760
document_note:: Algorithm Distillation (AD) is a technique developed by DeepMind scientists that allows transformers to "learn how to learn" in arbitrary RL environments without updating their weights. AD works by treating RL policy-learning as a sequence modeling problem and using a GPT architecture, a large dataset of training histories, a log-likelihood loss, and multi-episodic contexts to train the transformer. AD is capable of distilling any RL algorithm and is more data efficient than certain RL algorithms, such as A3C and DQN. It has implications for RL in terms of demonstrating the power of transformer methods and making RL algorithms more accessible to those with less compute power.
tags:: #[[neural networks]]

- Highlights first synced by [[Readwise]] [[Mar 6th, 2023]]
	- Using Algorithm Distillation (AD), DeepMind scientists trained transformers to "learn how to learn":
	- ![](https://pbs.twimg.com/media/Fl421HaacAALqGY.jpg) ([View Highlight](https://read.readwise.io/read/01gte2h3tvd5kdvg5bfq21961t))
	- TL;DR: A team from DeepMind trained transformers to: