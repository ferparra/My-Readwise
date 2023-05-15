title:: How Does a Large Languag... (highlights)
author:: [[@DanHollick on Twitter]]
full-title:: "How Does a Large Languag..."
category:: #tweets
url:: https://twitter.com/DanHollick/status/1646509271843225600

- Highlights first synced by [[Readwise]] [[May 1st, 2023]]
	- How does a Large Language Model like ChatGPT actually work?
	  
	  Well, they are both amazingly simple and exceedingly complex at the same time.
	  
	  Hold on to your butts, this is a deep dive ↓ https://t.co/s4j8SLbTv2 ([View Tweet](https://twitter.com/DanHollick/status/1646509271843225600))
		- **Note**: Thread
	- You can think of a model as calculating the probabilities of an output based on some input.
	  
	  In language models, this means that given a sequences of words they calculate the probabilities for the next word in the sequence.
	  
	  Like a fancy autocomplete. 
	  
	  ![](https://pbs.twimg.com/media/FtmTdmJaMAAu0E-.jpg) ([View Tweet](https://twitter.com/DanHollick/status/1646509280764497926))
	- To understand where these probabilities come from, we need to talk about something called a neural network.
	  
	  This is a network like structure where numbers are fed into one side and probabilities are spat out the other.
	  
	  They are simpler than you might think. https://t.co/e9X3EdTu6q ([View Tweet](https://twitter.com/DanHollick/status/1646509318802644994))
	- Imagine we wanted to train a computer to solve the simple problem of recognising symbols on a 3x3 pixel display.
	  
	  We would need a neural net like this:
	- Our input layer consists of 9 nodes called neurons - one for each pixel. Each neuron would hold a number from 1 (white) to -1 (black).
	  
	  Our output layer consists of 4 neurons, one for each of the possible symbols. Their value will eventually be a probability between 0 and 1. 
	  
	  ![](https://pbs.twimg.com/media/FtmTgypakAErT7E.png) ([View Tweet](https://twitter.com/DanHollick/status/1646509336406163457))
	- In between these, we have rows of neurons, called "hidden" layers. For our simple use case we only need two.
	  
	  Each neuron is connected to the neurons in the adjacent layers by a weight, which can have a value between -1 and 1. 
	  
	  ![](https://pbs.twimg.com/media/FtmThVWaEAAYQlD.jpg) ([View Tweet](https://twitter.com/DanHollick/status/1646509346652815361))
	- When a value is passed from the input neuron to the next layer its multiplied by the weight.
	  
	  That neuron then simply adds up all the values it receives,  squashes the value between -1 and 1 and passes it to each neuron in the next layer. 
	  
	  ![](https://pbs.twimg.com/media/FtmTh4naEAIFV4v.jpg) ([View Tweet](https://twitter.com/DanHollick/status/1646509355871899651))
	- The neuron in the final hidden layer does the same but squashes the value between 0 and 1 and passes that to the output layer.
	  
	  Each neuron in the output layer then holds a probability and the highest number is the most probable result. 
	  
	  ![](https://pbs.twimg.com/media/FtmTiaDacAcIG4u.jpg) ([View Tweet](https://twitter.com/DanHollick/status/1646509364222779392))
	- When we train this network, we feed it an image we know the answer to and calculate the difference between the answer and the probability the net calculated.
	  
	  We then adjust the weights to get closer to the expected result.
	  
	  But how do we know *how* to adjust the weights? https://t.co/X2SHyntYkE ([View Tweet](https://twitter.com/DanHollick/status/1646509472016375808))
	- I won't go into detail, but we use clever mathematical techniques called gradient descent and back propagation to figure out what value for each weight will give us the lowest error.
	  
	  We keep repeating this process until we are satisfied with the model's accuracy. https://t.co/FXgoe5ELOu ([View Tweet](https://twitter.com/DanHollick/status/1646509514672472066))
	- This is called a feed forward neural net - but this simple structure won't be enough to tackle the problem of natural language processing.
	  
	  Instead LLMs tend to use a structure called a transformer and it has some key concepts that unlock a lot of potential. 
	  
	  ![](https://pbs.twimg.com/media/FtmTryCacAA-Jv5.png) ([View Tweet](https://twitter.com/DanHollick/status/1646509525485391874))
	- First, lets talk about words.
	  
	  Instead of each word being an input, we can break words down into tokens which can be words, subwords, characters or symbols.
	  
	  Notice how they even include the space. https://t.co/1JJwrQt2mT ([View Tweet](https://twitter.com/DanHollick/status/1646509571035512835))
	- Much like in our model we represent the pixel value as a number between 0 and 1, these tokens also need to be represented as a number.
	  
	  We could just give each token a unique number and call it a day but there's another way we can represent them that adds more context. https://t.co/oqGjkREsUO ([View Tweet](https://twitter.com/DanHollick/status/1646509600206901251))
	- We can store each token in a multi-dimensional vector that indicates it's relationship to other tokens.
	  
	  For simplicity, imagine a 2D plane on which we plot the location of words. We want words with similar meanings to be grouped closer together.
	  
	  This is called an embedding. 
	  
	  ![](https://pbs.twimg.com/media/FtmTwtbaQAMOtKQ.png) ([View Tweet](https://twitter.com/DanHollick/status/1646509609405009922))
	- Embeddings help create relationships between similar words but they also capture analogies.
	  
	  For example the distance between the words dog and puppy should be the same as the distance between cat and kitten.
	  
	  We can also create embeddings for whole sentences. 
	  
	  ![](https://pbs.twimg.com/media/FtmTxLuaYAAvARE.png) ([View Tweet](https://twitter.com/DanHollick/status/1646509617084796931))
	- The first part of the transformer is to encode our input words into these embeddings.
	  
	  Those embeddings are then fed to the next process, called attention which adds even more context to embeddings.
	  
	  Attention is massively important in natural language processing. 
	  
	  ![](https://pbs.twimg.com/media/FtmTxoEaUActhpe.png) ([View Tweet](https://twitter.com/DanHollick/status/1646509625997668353))
	- Embeddings struggle to capture words with multiple meanings.
	  
	  Consider the two meanings of 'bank'. Humans derive the correct meaning based on the context of the sentence.
	  
	  'Money' and 'River' are contextually important to the word bank in each of these sentences. 
	  
	  ![](https://pbs.twimg.com/media/FtmTyJ0aMAIGPGs.png) ([View Tweet](https://twitter.com/DanHollick/status/1646509635904618496))
	- The process of attention looks back through the sentence for words that provide context to the word bank.
	  
	  It then re-weights the embedding so that the word bank is semantically closer to the word 'river' or 'money'. 
	  
	  ![](https://pbs.twimg.com/media/FtmTytdagAA5Tvo.png) ([View Tweet](https://twitter.com/DanHollick/status/1646509644679086082))
	- This attention process happens many times over to capture the context of the sentence in multiple dimensions.
	  
	  After all this, the contextualised embeddings are eventually passed into a neural net, like our simple one from earlier, that produces probabilities. ([View Tweet](https://twitter.com/DanHollick/status/1646509650458836996))
	- That is a massively simplified version of how an LLM like ChatGPT actually works. There is so much I've left out or skimmed over for the sake of brevity (this is the 20th tweet).
	  
	  If I left something important out or got some detail wrong, let me know. ([View Tweet](https://twitter.com/DanHollick/status/1646509653461991430))
	- I've been researching this thread on/off for ~6 months. Here are some of the best resources:
	  
	  Obviously this absolute unit of a piece by Stephen Wolfram which goes into much more detail than I have here:
	  
	  https://t.co/GV9tEeBTW9 ([View Tweet](https://twitter.com/DanHollick/status/1646509656486080513))
	- For something a bit more approachable, this @3blue1brown video series about how neural nets learn.
	  
	  There are some lovely graphics here, even if you don't follow all the maths.
	  
	  https://t.co/y91s8pgCKS ([View Tweet](https://twitter.com/DanHollick/status/1646509659271098369))
	- And @CohereAI's blog has some excellent pieces and videos explaining embeddings, attention and transformers.
	  
	  https://t.co/z7Hzjk9Tts
	  https://t.co/l4dd1C9WGw ([View Tweet](https://twitter.com/DanHollick/status/1646509662119030787))
	- There are tons more but that should keep you busy for a while.
	  
	  If you managed to read all the way down here, you might be heartened to know none of this was written by AI.
	  
	  I'm told it helps to remind you to retweet the original tweet. ([View Tweet](https://twitter.com/DanHollick/status/1646509665013084161))
	- You may now let go of your butts. ([View Tweet](https://twitter.com/DanHollick/status/1646509668414689281))
	- You can read the unrolled version here:
	  
	  https://t.co/aXQc3mjCZy ([View Tweet](https://twitter.com/DanHollick/status/1646547155342045185))