title:: "Imagine Learning a Text... (highlights)
author:: [[@astonzhangAZ on Twitter]]
full-title:: ""Imagine Learning a Text..."
category:: #tweets
url:: https://twitter.com/astonzhangAZ/status/1621545166049005568

- Highlights first synced by [[Readwise]] [[Feb 5th, 2023]]
	- "Imagine learning a textbook with no figures."
	  
	  Multimodal chain-of-thought (Multimodal-CoT) in Language Models
		- **Note**: Thread
	- Existing studies related to CoT reasoning are largely isolated in the language modality.
	  
	  Given inputs in different modalities, Multimodal-CoT decomposes multi-step problems into intermediate reasoning steps (rationale) and then infers the answer.
	  
	  [2/6] 
	  
	  ![](https://pbs.twimg.com/media/FoDiEV4akAAXKfV.jpg) ([View Tweet](https://twitter.com/astonzhangAZ/status/1621545169589014528))
	- Why Multimodal-CoT?
	  
	  Vision input is a wealth of information that was not fully exploited for CoT reasoning in the past.
	  
	  See an example where the baseline (without using vision features) fails to predict the right answer due to the misleading by hallucinated rationales.
	  
	  [3/6] 
	  
	  ![](https://pbs.twimg.com/media/FoDiJ8vaQAEQZVg.jpg) ([View Tweet](https://twitter.com/astonzhangAZ/status/1621545172516610053))
	- How Multimodal-CoT works:
	  
	  (i) Feed the model with language and vision inputs to generate rationales
	  (ii) Append the original language input with this generated rationale. Feed the updated language input with the original vision input to the model to infer the answer
	  
	  [4/6] 
	  
	  ![](https://pbs.twimg.com/media/FoDiNAWaYAIZBx7.jpg) ([View Tweet](https://twitter.com/astonzhangAZ/status/1621545175746232322))
	- Multimodal-CoT *under 1 billion parameters* outperforms the previous state-of-the-art LLM (GPT-3.5) by 16% (75.17%→91.68%) and even surpasses human performance on the ScienceQA benchmark.
	  
	  [5/6] 
	  
	  ![](https://pbs.twimg.com/media/FoDiP7maYAA5Sn6.jpg) ([View Tweet](https://twitter.com/astonzhangAZ/status/1621545177755308032))
	- Multimodal Chain-of-Thought Reasoning in Language Models
	  https://t.co/fkuLECPQj8
	  
	  Code & model:
	  https://t.co/8rMdf6L2ph
	  
	  Thank @lupantech for providing model info on ScienceQA!
	  [6/6] ([View Tweet](https://twitter.com/astonzhangAZ/status/1621545180980719616))