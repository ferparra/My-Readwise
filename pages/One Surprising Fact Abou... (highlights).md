title:: One Surprising Fact Abou... (highlights)
author:: [[@TivadarDanka on Twitter]]
full-title:: "One Surprising Fact Abou..."
category:: #tweets
url:: https://twitter.com/TivadarDanka/status/1531230948112470018

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- One surprising fact about calculus: differentiation can be inverted.
	  
	  An even more surprising fact: its inverse is integration!
	  
	  After reading this thread, you'll be amazed by the brilliance of Newton's calculus. ↓ ([View Tweet](https://twitter.com/TivadarDanka/status/1531230948112470018))
		- **Note**: Thread
	- Let's start at the basics!
	  
	  Suppose that we have a moving object. For simplicity, let's assume that it moves along a straight line.
	  
	  We can fully describe its dynamics with its time-distance function.
	  
	  For example, this is a constant velocity motion: 
	  
	  ![](https://pbs.twimg.com/media/FUAGb91VsAEm6i5.png) ([View Tweet](https://twitter.com/TivadarDanka/status/1531230955700072449))
	- As Newton discovered, the derivative of the time-distance function is its speed!
	  
	  In the case of a constant velocity motion, the speed is constant. (As properly reflected by its name.) 
	  
	  ![](https://pbs.twimg.com/media/FUAGcbMVsAAtGiK.png) ([View Tweet](https://twitter.com/TivadarDanka/status/1531230963203645441))
	- To sum up, speed is the derivative of distance.
	  
	  The question is if we only know the speed of our moving object, can we reconstruct the distance traveled? ([View Tweet](https://twitter.com/TivadarDanka/status/1531230966189989893))
	- For our constant velocity motion, this is easy to do: if an object is moving at speed v for time T, the total distance traveled is v⋅T.
	  
	  This quantity also coincides with the area under the time-speed graph. Is this a coincidence?
	  
	  No, as we shall see next. 
	  
	  ![](https://pbs.twimg.com/media/FUAGc7qUUAA8rDz.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1531230971982336000))
	- Does the area under the time-speed graph equal the distance traveled in the general case? 
	  
	  For instance, what happens when the time-speed plot looks something like this? 
	  
	  ![](https://pbs.twimg.com/media/FUAGdSkUEAATmwU.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1531230978424729600))
	- In this case, we can do a simple trick: partition the time interval [0, T] into smaller ones and approximate the object’s motion as a constant velocity motion on each of these intervals.
	  
	  Thus, we can reduce the general case to a special one that we have already seen. 
	  
	  ![](https://pbs.twimg.com/media/FUAGdrmVsAEkyCM.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1531230984879845377))
	- If the time intervals are sufficiently granular, the distance traveled will roughly match a constant velocity motion with the average speed in a given interval. 
	  
	  ![](https://pbs.twimg.com/media/FUAGeCeUAAAVyvR.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1531230990948962310))
	- In mathematical terms, we can approximate the total distance traveled with a finite sum. 
	  
	  ![](https://pbs.twimg.com/media/FUAGeZKUEAA0G8K.png) ([View Tweet](https://twitter.com/TivadarDanka/status/1531230997403955200))
	- Notice that this sum approximates the area under the time-speed graph as well!
	  
	  If we increase the granularity of the partition, this sum will converge to the true area under the curve.
	  
	  This is what we call integration. 
	  
	  ![](https://pbs.twimg.com/media/FUAGexkUEAA2oRo.png) ([View Tweet](https://twitter.com/TivadarDanka/status/1531231003875807233))
	- Notice that the integral represents the signed area, meaning that if the curve goes below the x-axis, the area is negative.
	  
	  This is not surprising since negative speed means backward movement. ([View Tweet](https://twitter.com/TivadarDanka/status/1531231006845329409))
	- To sum up once more, speed is the derivative of distance, and distance is the integral of speed.
	  
	  This is synthesized by the Newton-Leibniz formula, one of the pinnacle results in calculus. It clearly expresses that integration is the inverse of differentiation. 
	  
	  ![](https://pbs.twimg.com/media/FUAGfS_UsAAjoBs.png) ([View Tweet](https://twitter.com/TivadarDanka/status/1531231012306309120))
	- This is just the tip of the iceberg. I just released all the detailed explanations in the early access of my Mathematics of Machine Learning book. Check it out!
	  
	  Understanding math will make you a better engineer, and I want to guide you along the way.
	  
	  https://t.co/sqaja6yKb2 ([View Tweet](https://twitter.com/TivadarDanka/status/1531231015171072000))
	- Read the unrolled thread here:
	  
	  https://t.co/yc01dEkEFt ([View Tweet](https://twitter.com/TivadarDanka/status/1531231017691820032))