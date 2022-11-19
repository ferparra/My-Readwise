title:: In Progress on the Tldra... (highlights)
author:: [[@steveruizok on Twitter]]
full-title:: "In Progress on the Tldra..."
category:: #tweets
url:: https://twitter.com/steveruizok/status/1469788339024932873

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- in progress on the tldraw engine v2 https://t.co/bmJJSs1Jpr ([View Tweet](https://twitter.com/steveruizok/status/1469788339024932873))
		- **Note**: Thread
	- The fun part of this: all of the shapes you see here are "custom", insofar as they extend the "base" shapes that come for free with the library. 
	  
	  ![](https://pbs.twimg.com/media/FGW5v5fXwA08j0O.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1469788344095756292))
	- The even more fun part: these custom shapes are tiny. This pen shape has roughly 50 lines of code. A few extra properties, a pair of overrides for the shape's React components. 
	  
	  ![](https://pbs.twimg.com/media/FGW6TUHXoAc2Ylq.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1469788346436182016))
	- This is even more noticeable for the tools. Each tool is a state machine that responds to events passed to it while the tool is selected. These tools can be very complex, especially the selection tool. 
	  
	  ![](https://pbs.twimg.com/media/FGW7coxXsAUjVqA.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1469788352236900353))
	- However, that complex behavior is almost always the same for different tools that fit the pattern, so creating a "custom" draw tool means only light touches. Here's the whole custom "pen tool" in the example. 
	  
	  ![](https://pbs.twimg.com/media/FGW77gaXwAcAsRB.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1469788354451746818))
	- Compare with the whole custom "highlighter tool". Same behaviors, minor tweaks. 
	  
	  ![](https://pbs.twimg.com/media/FGW8EwSWQAYtzHx.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1469788358515871750))
	- Of course, if you wanted to write your own tools and shapes entirely from scratch, there are "lower" base classes that you could extend from. But in general the abstractions are very useful—box, dot, draw, polygon, etc—and chances are your idea falls into one of them. ([View Tweet](https://twitter.com/steveruizok/status/1469788360348737537))