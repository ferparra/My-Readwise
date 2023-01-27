title:: YouTube (highlights)
author:: [[youtube.com]]
full-title:: "YouTube"
category:: #articles
url:: https://www.youtube.com/

- Highlights first synced by [[Readwise]] [[Dec 24th, 2022]]
	- 2:36 Notes 
	  10:12 Chords
	  11:58 Major and Minor 
	  15:36 The Number System 
	  20:29 Inversions 
	  23:59 Melodies 
	  27:26 Rhythm
- New highlights added [[Dec 25th, 2022]] at 1:47 AM
	- 1 : The patheless path 
	  2 : Someday is today 
	  3 : Beyond wealth 
	  4 : The 3 alarms 
	  5 : The art of business of online writing 
	  6 : The 7 habits of highly effective people 
	  7 : Scorecard marketing 
	  8 : What we owe the future 
	  9 : The go-giver 
	  10 : The luck factor 
	  11 : The way of the superior man 
	  12 : $100M offers 
	  13 : Sapiens 
	  14 : The surrender experiment 
	  15 : The seven husbands of Evelyn Hugo
- New highlights added [[Jan 23rd, 2023]] at 3:31 PM
	- Links:
	- Attention is All You Need paper: https://arxiv.org/abs/1706.03762
	- Chapters:
	  00:00:00 intro: ChatGPT, Transformers, nanoGPT, Shakespeare
	  baseline [[language modeling]], code setup
	  00:07:52 reading and exploring the data
	  00:09:28 tokenization, train/val split
	  00:14:27 data loader: batches of chunks of data
	  00:22:11 simplest baseline: bigram language model, loss, generation
	  00:34:53 training the bigram model
	  00:38:00 port our code to a script
	  Building the "[[self-attention]]"
	  00:42:13 version 1: averaging past context with for loops, the weakest form of aggregation
	  00:47:11 the trick in [[self-attention]]: [[matrix multiply]] as weighted aggregation
	  00:51:54 version 2: using [[matrix multiply]]
	  00:54:42 version 3: adding [[softmax]]
	  00:58:26 minor code cleanup
	  01:00:18 positional encoding
	  01:02:00 THE CRUX OF THE VIDEO: version 4: self-attention
	  01:11:38 note 1: attention as communication
	  01:12:46 note 2: attention has no notion of space, operates over sets
	  01:13:40 note 3: there is no communication across batch dimension
	  01:14:14 note 4: [[encoder blocks]] vs. [[decoder blocks]]
	  01:15:39 note 5: attention vs. self-attention vs. cross-attention
	  01:16:56 note 6: "scaled" self-attention. why divide by sqrt(head_size)
	  Building the Transformer
	  01:19:11 inserting a single self-attention block to our network
	  01:21:59 multi-headed self-attention
	  01:24:25 feedforward layers of transformer block
	  01:26:48 residual connections
	  01:32:51 [[layernorm]] (and its relationship to our previous [[batchnorm]])
	  01:37:49 scaling up the model! creating a few variables. adding dropout
	  Notes on Transformer
	  01:42:39 encoder vs. decoder vs. both (?) [[Transformers]]
	  01:46:22 super quick walkthrough of nanoGPT, batched multi-headed self-attention
	  01:48:53 back to ChatGPT, [[GPT-3]], [[pre-training]] vs. [[fine-tuning]], RLHF
	  01:54:32 conclusions