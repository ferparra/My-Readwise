title:: Thought-Provocative New... (highlights)
author:: [[@martin_gorner on Twitter]]
full-title:: "Thought-Provocative New..."
category:: #tweets
url:: https://twitter.com/martin_gorner/status/1599755684941557761

- Highlights first synced by [[Readwise]] [[Dec 6th, 2022]]
	- Thought-provocative new paper from @geoffreyhinton: what if we could replace backpropagation with something better? 
	  
	  ![](https://pbs.twimg.com/media/FjN5PduXoAA0ruC.jpg) ([View Tweet](https://twitter.com/martin_gorner/status/1599755684941557761))
		- **Note**: Thread
	- @geoffreyhinton I seems very unlikely that the human brain uses back propagation to learn. There is little evidence of backprop mechanics in biological brains (no error derivatives propagating backwards, no storage of neuron activities to use in a packprop pass, ...). 
	  
	  ![](https://pbs.twimg.com/media/FjN5fs7XgAIH1WQ.jpg) ([View Tweet](https://twitter.com/martin_gorner/status/1599755910271803394))
	- @geoffreyhinton Also, the brain can learn from a continuous stream of incoming data and does not need to stop to run a backprop pass. Yes, sleep is beneficial for learning somehow, but we can learn awake too. 
	  
	  ![](https://pbs.twimg.com/media/FjN5q-zWIAI2mYL.jpg) ([View Tweet](https://twitter.com/martin_gorner/status/1599756096516026368))
	- @geoffreyhinton So what other way is there to update neural network weights to achieve a given objective ? Hinton suggests a mechanism based on two forward passes: the Forward Forward algorithm.
	  https://t.co/fj4DnJfNqp ([View Tweet](https://twitter.com/martin_gorner/status/1599756582811623424))
	- @geoffreyhinton Let's take a 2 layer dense neural network and implement an image classifier. The regular, backprop way of training is to push data through the network, compare the outcome to labels, compute a loss fn, differentiate it and update weights through backprop. 
	  
	  ![](https://pbs.twimg.com/media/FjN7TG8WQAA2cAS.jpg) ([View Tweet](https://twitter.com/martin_gorner/status/1599758002349039616))
	- @geoffreyhinton Instead in FF, we merge labels and data in one vector, the "good data", and then generate "bad data" by merging input images with the wrong labels. Here is what this could look like on MNIST handwritten digits: 
	  
	  ![](https://pbs.twimg.com/media/FjN8-XjWYAcCRlb.jpg) ([View Tweet](https://twitter.com/martin_gorner/status/1599759770608549888))
	- @geoffreyhinton And now, we want each network layer to feel "excited" about the good data, i.e. exhibit high activations, and on the contrary have low activations on "bad data". 
	  
	  ![](https://pbs.twimg.com/media/FjN_PYpWAAA2GWg.jpg) ([View Tweet](https://twitter.com/martin_gorner/status/1599762227263074304))
	- @geoffreyhinton That's very easy to do, compute the sum of squared activations in a layer and maximize it on "good data" while minimizing it on "bad data". This is purely within one layer, so no backprop is necessary, just a derivative of the function performed by the layer itself (easy). ([View Tweet](https://twitter.com/martin_gorner/status/1599762361413292032))
	- @geoffreyhinton When chaining multiple layers, you want to avoid seeing hight activations just because you pumped in high inputs from a very excited previous layer. So layer activations are normalized (divided by the norm of the activation vector) between layers. 
	  
	  ![](https://pbs.twimg.com/media/FjOAFjrXgAc8YDW.jpg) ([View Tweet](https://twitter.com/martin_gorner/status/1599763215851737090))
	- @geoffreyhinton In short, the activation vector retains its direction between layers, but its norm is reset to 1 before passing it to the next layer.
	  
	  The training then alternates good data and bad data, and performs weight updates in each layer accordingly. ([View Tweet](https://twitter.com/martin_gorner/status/1599763383007383552))
	- @geoffreyhinton How about inference ? Again concatenate an MNIST digit with a label, any label, feed it through the network and see if the network as a whole is exited about it. You will have to do it for all image-label combinations though. 
	  
	  ![](https://pbs.twimg.com/media/FjOBqs6WYAA3kfZ.jpg) ([View Tweet](https://twitter.com/martin_gorner/status/1599764917589921792))
	- @geoffreyhinton Even better, the [[Forward-Forward]] algorithm lends itself quite naturally to [[self-supervised learning]]. You can learn about "digits" by feeding non-digits as "bad data" (example non-digit generation from paper). Such a network can then be fine-tuned on a downstream task. 
	  
	  ![](https://pbs.twimg.com/media/FjOCYPNXEAQKpNg.jpg) ([View Tweet](https://twitter.com/martin_gorner/status/1599765732312555523))
	- @geoffreyhinton Additional benefit: [[Forward-Forward]] training does NOT require that the entire forward pass be differentiable. There can be a non-differentiable black box in the middle, the FF algorithm does not care! With backprop, you would need to reach for slow Reinforcement Learning here. 
	  
	  ![](https://pbs.twimg.com/media/FjODtiQWQAAtLLc.jpg) ([View Tweet](https://twitter.com/martin_gorner/status/1599767270409969665))
	- @geoffreyhinton And finally, Hinton points out that FF is easily implementable with very power-efficient analog circuits. This could allow us to run very large language models in a fraction of a Watt!
	  Read the paper for more Hinton's thoughts I have omitted. https://t.co/fj4DnIYKop ([View Tweet](https://twitter.com/martin_gorner/status/1599768066375962625))