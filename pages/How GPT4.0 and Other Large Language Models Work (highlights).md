title:: How GPT4.0 and Other Large Language Models Work (highlights)
author:: [[weaviate.io]]
full-title:: "How GPT4.0 and Other Large Language Models Work"
category:: #articles
url:: https://weaviate.io/blog/what-are-llms
tags:: #[[gpt-4]] #[[LLMs]]

- Highlights first synced by [[Readwise]] [[Apr 7th, 2023]]
	- a huge reason why these models are fascinating is because of their ability to paraphrase and articulate a vast general knowledge base by generating human-like phrases and language. If ChatGPT had simply “copy-pasted” content from the most relevant source to answer our questions, it would be far less impressive a technology. In the case of language models, their ability to summarize, paraphrase and compress source knowledge into realistic language is much more impressive. Ted Chiang captures this exact concept eloquently in his recent article [ChatGPT Is a Blurry JPEG of the Web](https://www.newyorker.com/tech/annals-of-technology/chatgpt-is-a-blurry-jpeg-of-the-web). ([View Highlight](https://read.readwise.io/read/01gx9sm1xatw0mnxprdfs51h35))
	- ![books](https://weaviate.io/assets/images/books-77398afc1da9251e09375fc1a6c6c392.png) ([View Highlight](https://read.readwise.io/read/01gx9sm5vc9h4dy8nvjmy38wv2))
	- This explains why LLMs know something about basically everything but it still doesn’t explain how they articulate this knowledge with human-like responses. The question then arises, what is the point of all this reading!? Are LLMs trying to comprehend what’s being read? Are they trying to break apart and learn the logic behind the concepts they are reading so they can piece back together concepts on demand upon questioning - as a student preparing for an exam would? Perhaps, but not quite in the way that humans learn and understand from reading. The answer to these questions lies in their name: “Language Model”. **LLMs are trying to build a statistical model of the language they are reading.** ([View Highlight](https://read.readwise.io/read/01gx9smmfhyg87en9vggmddapy))
	- Humans can reason and understand language at increasingly deeper levels of meaning. Here are some reasons, in order of increasing lingual comprehension, that explains why the latter phrase didn’t occur to many:
	  
	  1.  You’ve heard the former phrase before, whereas you’ve never heard the latter; one combination of words is common and familiar, while the other is not.
	    
	  2.  You know that feathers can go in caps, however feathers don’t go on cats! Even on a superficial level, one makes sense based on our understanding and knowledge of the world, and the other does not!
	    
	  3.  You can understand the deeper meaning behind the prior phrase as accomplishing something to be proud of, whereas the latter doesn’t have any deeper meaning behind it.
	    
	  4.  If there were a deeper meaning to be interpreted, such as irony or sarcasm that was subtley woven into the phrase, humans would also be able to comprehend that. ([View Highlight](https://read.readwise.io/read/01gx9sn1wmfvh8njk99zgj1c68))
	- At a high level, this is what LLMs like OpenAI’s GPT 4.0, Meta’s LLaMA, and Google’s LaMDA are trying to achieve from their vast amounts of reading. They are trying to measure which words are often used together across different types of texts. This allows them to quantify which combination of words and phrases are common and which ones aren’t - allowing them to emulate the first level of reasoning above. ([View Highlight](https://read.readwise.io/read/01gx9sn7tvnewce4e61t4c748b))
	- As Geoff Hinton, sometimes referred to as the “Godfather of Deep Learning”, recently put it:
	  
	  > “LLMs do not do pattern matching in the sense that most people understand it. They use the data to create huge numbers of features and interactions between features such that these interactions can predict the next word.”
	  
	  These features are preserved in the LLM’s parameters (what I like to think of as the brains of the model), which GPT 3.0 has 175 billion of - it would require 800GB to even store these parameters. Now whether you consider passing a prompt through these parameters and getting an LLM to generate the most likely response word by word as requiring an “understanding” of the underlying text in the same way that a human would “understand” a question prior to formulating an answer, is an open question that I leave to the reader to ponder! ([View Highlight](https://read.readwise.io/read/01gx9sngtybvpxy23syrypwa4w))
	- Geoff has another great take on this:
	  
	  > “I believe that factoring the discrete symbolic information into a very large number of features and interactions ***IS*** intuitive understanding and that this is true for both brains and LLMs even though they may use different learning algorithms for arriving at these factorizations.”
	  
	  Another limitation of these models, to keep in mind when thinking about whether LLMs understand what they read, is that they are only “language” models whereas humans have the benefit of putting together and choosing between multiple modalities of understanding, including language, visual, aural, mathematical, physical etc. An example of this is that LLMs are not good at solving mathematical problems since they cannot distill and learn the rules of algebra from reading a math textbook - they don’t have a “math mode” that overrides their “language mode” when tasked with solving even the easiest of math problems. So it’s really not fair to compare an LLM’s uni-modal comprehension to that of a humans full multi-modal comprehension capabilities. Efforts are being made to make these models understand other modalities of data - for example with the release of GPT 4.0 last week, ChatGPT can now understand images that you pass in and can couple this image understanding with its language understanding. ([View Highlight](https://read.readwise.io/read/01gx9snwf52pbqttctmk5xj648))