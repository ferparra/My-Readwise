title:: Machine Learning Models... (highlights)
author:: [[@mrdbourke on Twitter]]
full-title:: "Machine Learning Models..."
category:: #tweets
url:: https://twitter.com/mrdbourke/status/1603155487758856193

- Highlights first synced by [[Readwise]] [[Dec 17th, 2022]]
	- Machine learning models can be so good they can help you improve your dataset/labels
	  
	  Created a @weights_biases Table to index the top 100 “most wrong” predictions on Nutrify's test set.
	  
	  Even though the top-1 prediction is wrong, the model often gets it right within the top-5. 
	  
	  ![](https://pbs.twimg.com/media/Fj-M9b6VIAEMAkw.jpg) ([View Tweet](https://twitter.com/mrdbourke/status/1603155487758856193))
		- **Note**: Thread
	- Going to use this to improve the labels/retrain a model.
	  
	  Been playing around with VQA (visual question answering) and vision-language models such as BLIP to automatically take care of some of the easier samples. ([View Tweet](https://twitter.com/mrdbourke/status/1603155491185602560))
	- For example:
	  • encode image, encode text of top 5
	  • perform similarity comparison 
	  • automatically relabel based on similarity comparison + predictions + true label
	  • send confusing samples to human (me) 
	  
	  Haven’t figured the workflow fully out yet but it looks promising. ([View Tweet](https://twitter.com/mrdbourke/status/1603155493349826560))
	- Similar to this:
	  https://t.co/uLP95pdZku ([View Tweet](https://twitter.com/mrdbourke/status/1603155495652450304))