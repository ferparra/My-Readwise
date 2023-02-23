title:: The Adam Optimizer Is At... (highlights)
author:: [[@DrJimFan on Twitter]]
full-title:: "The Adam Optimizer Is At..."
category:: #tweets
url:: https://twitter.com/DrJimFan/status/1625920773042089984

- Highlights first synced by [[Readwise]] [[Feb 16th, 2023]]
	- The Adam optimizer is at the heart of modern AI. Researchers have been trying to dethrone Adam for years.
	  
	  How about we ask a machine to do a better job? @GoogleAI uses evolution to discover a simpler & efficient algorithm with remarkable features.
	  
	  It’s just 8 lines of code: 🧵 
	  
	  ![](https://pbs.twimg.com/media/FpBuUwJakAAodrF.jpg) ([View Tweet](https://twitter.com/DrJimFan/status/1625920773042089984))
		- **Note**: Thread
	- The discovered “Lion” optimizer is able to boost the accuracy of Vision Transformers (ViT) by up to 2% on ImageNet, reduce training compute by up to 2.3x for diffusion models, and achieve comparable performance on LLMs. It is more memory-efficient compared to human designs.
	  
	  2/ 
	  
	  ![](https://pbs.twimg.com/media/FpBuVNCacAA4nsr.jpg) ([View Tweet](https://twitter.com/DrJimFan/status/1625920779354521606))
	- Remarkably, the evolutionary search decides that the SIGN of gradient is all you need. For example, if the gradient is [-0.31, 0.43, -0.21], Lion turns it into [-1, 1, -1] for the update vector. This is counter-intuitive and nontrivial for human researchers to come up with.
	  
	  3/ ([View Tweet](https://twitter.com/DrJimFan/status/1625920782332489729))
	- I want to highlight that this paper is a great demonstration of a *scalable* symbolic AI system. There are prior works that propose neural network-based, learned meta-optimizers. But Lion is a much simpler symbolic form that is interpretable and lightweight to incorporate.
	  
	  4/ 
	  
	  ![](https://pbs.twimg.com/media/FpBuVrjakAIEkPJ.jpg) ([View Tweet](https://twitter.com/DrJimFan/status/1625920788091248640))
	- Paper: https://t.co/oq1097MRB8
	  Authors: @XiangningChen, @crazydonkey200, Da Huang, Esteban Real, Kaiyuan Wang, Yao Liu, Hieu Pham, Xuanyi Dong, Thang Luong, Cho-Jui Hsieh, Yifeng Lu, @quocleix. 
	  
	  Follow me for more deep dives ;) https://t.co/junzQA1CkV ([View Tweet](https://twitter.com/DrJimFan/status/1625920791983554560))