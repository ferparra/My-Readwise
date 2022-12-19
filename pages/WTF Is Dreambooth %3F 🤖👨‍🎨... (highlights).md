title:: WTF Is Dreambooth ? 🤖👨‍🎨... (highlights)
author:: [[@PellegrinPierre on Twitter]]
full-title:: "WTF Is Dreambooth ? 🤖👨‍🎨..."
category:: #tweets
url:: https://twitter.com/PellegrinPierre/status/1592613303632551936

- Highlights first synced by [[Readwise]] [[Dec 6th, 2022]]
	- WTF is Dreambooth ? 🤖👨‍🎨
	  
	  Maybe you tried some AI to generate images but it lacks personalization. This was until... Dreambooth ✨
	  
	  This brand-new AI let you generates photos of you like Dall-E or MidJourney 🤖
	  
	  🛠 How it works ? (Part. 1/3)
	  
	  A THREAD 👇🧵 ([View Tweet](https://twitter.com/PellegrinPierre/status/1592613303632551936))
		- **Note**: Thread
	- Dall-e, ImageGen, Midjourney, these technologies have multiplied and allow to obtain impressive results.
	  
	  For example by writing the sentence below we can generate the following image:
	  
	  "Teddy bears working on new AI research underwater with 1990s technology" 
	  
	  ![](https://pbs.twimg.com/media/FhoZXX8UAAABI46.png) ([View Tweet](https://twitter.com/PellegrinPierre/status/1592613313023647744))
	- These algorithms may work if you want to generate images of celebrity faces but will not work with your own face.
	  
	  Why? These AIs do not know you and have not been trained to identify you. Hence, they won't know my name if I type it in text input. ([View Tweet](https://twitter.com/PellegrinPierre/status/1592613315934420994))
	- Until one day a team of Google researchers published a paper on a revolutionary method called Dreambooth. ✨
	  
	  I planned to write 3 threads for a complete presentation:
	  👉 How it works technically🛠
	  👉 How to train it with your own images🤖
	  👉 How to make money with Dreambooth🤑 ([View Tweet](https://twitter.com/PellegrinPierre/status/1592613318388199424))
	- 🛠 How it works ?
	  
	  The idea is to use a model that has been pre-trained on billions of data points and then re-trained (or fine-tuned) on a few images of an object or a person. ([View Tweet](https://twitter.com/PellegrinPierre/status/1592613320896368640))
	- This will allow the model to learn to link a unique identifier (your name) to a specific subject (your face). In our case, the pre-trained model is called Stable Diffusion. ([View Tweet](https://twitter.com/PellegrinPierre/status/1592613323429715974))
	- Once the subject and its identifier have been learned by the model, it can be used to synthesize realistic images contextualized in different scenes 
	  
	  ![](https://pbs.twimg.com/media/FhoZYZPVEAAKki0.jpg) ([View Tweet](https://twitter.com/PellegrinPierre/status/1592613331382124544))
	- The use of Dreambooth is divided into two parts:
	  
	  👉 Fine-tuning : part where we re-train Stable Diffusion with our own images.
	  
	  👉 Inference : using our model to obtain a result ([View Tweet](https://twitter.com/PellegrinPierre/status/1592613334334914561))
	- Fine-tuning 🤖
	  
	  We give as input to the model some images of a subject, for example a dog with the identifier "[V]" and say that it is a dog.
	  
	  We re-train the model, and we get a new model that now understands what "[V]" is, it is a dog that looks like the pictures we provided. ([View Tweet](https://twitter.com/PellegrinPierre/status/1592613336822136833))
	- Inference 🔮
	  
	  With our new model we can write as input "A [V] dog in the beach" and Dreambooth will generate a picture of our cute little dog at the beach. 🐶 ([View Tweet](https://twitter.com/PellegrinPierre/status/1592613339292573697))
	- How Dreambooth learn who you are ?
	  
	  • It tries to reconstruct the image of [V] dog.
	  • And generates images of the subject class, in our example: a dog, thanks to Stable Diffusion.
	  
	  Dreambooth understand similarities and differences between the [V] dog and all the other dogs. 
	  
	  ![](https://pbs.twimg.com/media/FhoZZTLVQAAR42F.jpg) ([View Tweet](https://twitter.com/PellegrinPierre/status/1592613345953124354))
	- Then, Dreambooth will get the images from your dataset, reduce their size to 64x64 pixels and train itself to enlarge the image. It is this process that allows the model to maintain high fidelity.
	  
	  Want to go further in technical details ? 👇
	  https://t.co/yMiA9SXeV5 ([View Tweet](https://twitter.com/PellegrinPierre/status/1592613348914253824))
	- Next week I'll post a tutorial to teach you how to generate images of yourself 📆
	  
	  Don't hesitate to subscribe to my newsletter to receive it in your inbox 👇
	  
	  https://t.co/FsojQFJ3Dt ([View Tweet](https://twitter.com/PellegrinPierre/status/1592613351447613440))