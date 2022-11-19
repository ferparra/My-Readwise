title:: Let's Rethink Speech Rec... (highlights)
author:: [[@sanchitgandhi99 on Twitter]]
full-title:: "Let's Rethink Speech Rec..."
category:: #tweets
url:: https://twitter.com/sanchitgandhi99/status/1585313347943079938

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Let's rethink Speech Recognition - 1% WER on LibriSpeech is near perfect performance on audiobooks, but what else?
	  
	  Introducing the End-to-end Speech Benchmark (ESB), for evaluating ASR systems on different datasets, domains and conditions. A thread (1/N)
	  
	  https://t.co/uOiKfFEEmi 
	  
	  ![](https://pbs.twimg.com/media/FgAqFYNVIAwQozQ.jpg) ([View Tweet](https://twitter.com/sanchitgandhi99/status/1585313347943079938))
		- **Note**: Thread
	- ASR research is progressing at great pace. However, systems are typically trained and evaluated on LibriSpeech (LS), an extremely clean dataset derived from audiobook recordings. SoTA on LS is now as low as 1.4% WER! 🤯 
	  
	  ![](https://pbs.twimg.com/media/FgAqF-kVIAcUB56.jpg) ([View Tweet](https://twitter.com/sanchitgandhi99/status/1585313356176498691))
	- So how do they do it? 🤔 Such systems optimise for LS performance with LS-specific model architectures and LS-specific pre-/post-processing. This LS-specific tuning yields systems that transfer poorly to other datasets and domains. ([View Tweet](https://twitter.com/sanchitgandhi99/status/1585313359133483016))
	- With ESB, we aim to encourage more generalisable speech systems. ESB consists of 8 speech recognition datasets, capturing a broad range of domains, acoustic conditions, speaking styles and transcription requirements. 
	  
	  ![](https://pbs.twimg.com/media/FgAqGiDVIAQtQHm.png) ([View Tweet](https://twitter.com/sanchitgandhi99/status/1585313366532235270))
	- We adopt an open-source and open-science approach by considering datasets are accessible and freely available 🤗
	  
	  All the ESB datasets can be downloaded in just one line of code using Hugging Face datasets: 
	  
	  ![](https://pbs.twimg.com/media/FgAqHCkVIBIyAxk.png) ([View Tweet](https://twitter.com/sanchitgandhi99/status/1585313373423476736))
	- To encourage systems capable of predicting formatted text, we retain all punctuation and casing in the ESB transcriptions and our WER calculation:
	  
	  Ref:     We   are   going   .
	  Pred:   we   are   going   ?
	  Eval:    ❌   ✅     ✅   ❌
	  => 50% WER ([View Tweet](https://twitter.com/sanchitgandhi99/status/1585313376095248390))
	- ESB requires the following three attributes to be consistent across all datasets:
	  • Model architecture
	  • Data pre-/post-processing
	  • Training and evaluation algorithms (e.g. for hyper-parameter tuning, selecting the best checkpoint for evaluation) ([View Tweet](https://twitter.com/sanchitgandhi99/status/1585313378603442178))
	- => ESB favours systems that can be applied independently across speech recognition domains with no a-priori knowledge of the data distributions. ([View Tweet](https://twitter.com/sanchitgandhi99/status/1585313381208104969))
	- There is no restriction on:
	  • The type of system: any system that takes audio as inputs and outputs text is eligible to participate
	  • The training data: submissions may use as much pre-training and fine-tuning data as they wish, be it public or private ([View Tweet](https://twitter.com/sanchitgandhi99/status/1585313383770824719))
	- => ESB is designed to be as flexible as possible in this regard, encouraging submissions from both academic and production settings. ([View Tweet](https://twitter.com/sanchitgandhi99/status/1585313386341933056))
	- To demonstrate ESB, we performed baseline experiments with five different E2E approaches, including:
	  🥇 Whisper from @OpenAI
	  🥈 Conformer RNN-T from @NVIDIAAI
	  🥉 Wav2Vec2 from @MetaAI 
	  
	  ![](https://pbs.twimg.com/media/FgAqIG4VIAAze1L.png) ([View Tweet](https://twitter.com/sanchitgandhi99/status/1585313392906018818))
	- Submitting to ESB is straightforward! Upload predictions for the ESB test sets to the following Space for scoring and automatic placement on the leaderboard: https://t.co/BAcqDljVsu ([View Tweet](https://twitter.com/sanchitgandhi99/status/1585313396399874048))
	- We believe that ESB offers a benchmark for developing improved speech recognition systems. We open the benchmark to the community and welcome submissions 🤗 ([View Tweet](https://twitter.com/sanchitgandhi99/status/1585313398966788101))
	- Many thanks to @huggingface @PatrickPlaten @srush_nlp @polinaeterna @albertzeyer @_jongwook_kim @HaseoX94 @ParcolletT @ChrisWTanner @shinjiw_at_cmu and @ChanghanWang among others! ([View Tweet](https://twitter.com/sanchitgandhi99/status/1585313401835692037))