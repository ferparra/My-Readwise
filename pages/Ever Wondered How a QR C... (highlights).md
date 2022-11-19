title:: Ever Wondered How a QR C... (highlights)
author:: [[@DanHollick on Twitter]]
full-title:: "Ever Wondered How a QR C..."
category:: #tweets
url:: https://twitter.com/DanHollick/status/1570040185500626947

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Ever wondered how a QR code works?  
	  No, me neither but it's low-key fascinating.
	  
	  (Warning, there is some extremely nerdy shit here.👇 ) 
	  
	  ![](https://pbs.twimg.com/media/FcnnOeBakAI4TbP.png) ([View Tweet](https://twitter.com/DanHollick/status/1570040185500626947))
		- **Note**: Thread
	- The Quick Response code was invented by a subsidiary of Toyota to track parts across the manufacturing process.
	  
	  Barcodes were proving inadequate - they can only be read at certain angles and didn't store much data relative to their size
	  
	  The QR code solves those issues and more 
	  
	  ![](https://pbs.twimg.com/media/FcnnO46acAE_zAB.png) ([View Tweet](https://twitter.com/DanHollick/status/1570040193742434304))
	- The most distinctive thing about a QR code are these cube shapes, called Finder Patterns, that help your reader detect the code.
	  
	  The smaller fourth cube, the Alignment Pattern, orientates the code so it can be at any angle and the reader will still know which way is up. 
	  
	  ![](https://pbs.twimg.com/media/FcnnPZZacAALNbh.png) ([View Tweet](https://twitter.com/DanHollick/status/1570040203825549313))
	- You've probably never noticed but every QR code has these alternating black and white dots called the Timing Pattern. 
	  
	  These tell the reader how big a single module is and how big the whole QR code is - known as the version.
	  
	  Version 1: Smallest
	  Version 40: Biggest 
	  
	  ![](https://pbs.twimg.com/media/FcnnP9dacAEoEJL.png) 
	  
	  ![](https://pbs.twimg.com/media/FcnnQSKaUAAhOOW.png) ([View Tweet](https://twitter.com/DanHollick/status/1570040218476216320))
	- Information about the format is stored in these two strips near the Finder patterns. 
	  
	  It's stored twice so its readable even when QR code is partially obscured. (You'll notice that this is a recurring theme.) 
	  
	  ![](https://pbs.twimg.com/media/FcnnQ0BakAALV15.png) ([View Tweet](https://twitter.com/DanHollick/status/1570040227640803328))
	- This stores three crucial pieces of information:
	- First, error correction - what is it?
	  
	  Essentially, it dictates how much redundant information is stored in the code to ensure it remains readable even when part of it is missing. 
	  
	  ![](https://pbs.twimg.com/media/FcnnRycaUAI6Ux9.png) ([View Tweet](https://twitter.com/DanHollick/status/1570040244107644929))
	- This is pretty amazing - If your code is outdoors you can choose a higher redundancy level to make sure it still functions when obscured.
	  
	  (try it) 
	  
	  ![](https://pbs.twimg.com/media/FcnnSUnagAMUQhY.png) ([View Tweet](https://twitter.com/DanHollick/status/1570040253184094213))
	- Second, the mask - what's that? 
	  
	  Well, QR readers work best when there are the same amount of white and black areas. 
	  
	  But the data might not play ball so a mask is used to even things out. 
	  
	  ![](https://pbs.twimg.com/media/FcnnSz8akAI80Vu.png) ([View Tweet](https://twitter.com/DanHollick/status/1570040261950205954))
	- When a mask is applied to the code anything that falls under the dark part of the mask is inverted.
	  
	  A white area becomes black and black area becomes white. https://t.co/hyrpaptpH2 ([View Tweet](https://twitter.com/DanHollick/status/1570040325103849473))
	- There are 8 standard patterns which are applied one by one.
	  
	  The pattern that achieves the best result is used and that info is stored so the reader can unapply the mask. 
	  
	  ![](https://pbs.twimg.com/media/FcnnXIjaAAANy9c.png) ([View Tweet](https://twitter.com/DanHollick/status/1570040335841243139))
	- Finally we get to the actual data. 
	  
	  Weirdly, the data starts at the bottom-right corner and winds back up like pictured. 
	  
	  It almost doesn't matter where it starts because it can be read at any angle. 
	  
	  ![](https://pbs.twimg.com/media/FcnnXo_aEAACmw0.png) ([View Tweet](https://twitter.com/DanHollick/status/1570040344309551104))
	- The first chunk of information here tells the reader what mode the data was encoded in and the second tells it the length.
	  
	  In our case each character takes up 8 bit chunks, otherwise known as bytes, and there are 24 of them. 
	  
	  ![](https://pbs.twimg.com/media/FcnnYJcaUAI5WFF.png) ([View Tweet](https://twitter.com/DanHollick/status/1570040354866626560))
	- There is still a bunch of left over space after our data. 
	  
	  This is where the error correction information is stored so that it can be read if partially obscured. The way this works is actually really really complex so I'll leave that out.
	  
	  That's basically it! 
	  
	  ![](https://pbs.twimg.com/media/FcnnYveacAQNKWQ.png) ([View Tweet](https://twitter.com/DanHollick/status/1570040363586564098))
	- For the absolute nerds who made it here, a fun fact: 
	  
	  Perhaps the coolest thing about QR codes is that Denso Wave, the company that invented them, never exercised their patent and released the technology for free!
	  
	  https://t.co/bcX94ghLNi ([View Tweet](https://twitter.com/DanHollick/status/1570040367273365506))
	- Apparently, to maximise engagement, I'm supposed to link the original tweet here and encourage you to retweet it. https://t.co/uIETZwoiab ([View Tweet](https://twitter.com/DanHollick/status/1570040370150641664))
	- You can check out the unrolled version here:
	  https://t.co/dJHcPyFTS7 ([View Tweet](https://twitter.com/DanHollick/status/1570043237104234501))