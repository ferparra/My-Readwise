title:: Make Your Code Faster Wi... (highlights)
author:: [[@mhevery on Twitter]]
full-title:: "Make Your Code Faster Wi..."
category:: #tweets
url:: https://twitter.com/mhevery/status/1628249257462607872

- Highlights first synced by [[Readwise]] [[Feb 25th, 2023]]
	- Make your code faster with Bloom filters. They are like HashMaps but smaller and allow you to short-circuit more expensive operations.
	  
	  🧵🪡🧶 
	  
	  ![](https://pbs.twimg.com/media/Fpi0EJTacAE5iey.jpg) ([View Tweet](https://twitter.com/mhevery/status/1628249257462607872))
		- **Note**: Thread
	- Imagine you have to do an expensive search operation for a KEY. You also know the most likely outcome is that the KEY will not be found. Such operations can’t be skipped on the off chance that the KEY is found.
	  
	  A bloom filter allows you to skip such work 
	  
	  ![](https://pbs.twimg.com/media/Fpi0E7aacAEPTwg.jpg) ([View Tweet](https://twitter.com/mhevery/status/1628249268644646912))
	- A bloom filter is a probabilistic data structure that can answer if a key is NOT present.
	  
	  bloomFilter.test(KEY):
	- Bloom filters use a hash() to convert KEY -> number.
	  
	  The number is then modulo bit array size and used to set a bit in bit-array.
	  
	  NOTE: we are talking bits => 1 byte = 8 bits => memory efficient 
	  
	  ![](https://pbs.twimg.com/media/Fpi0GR8acAAakSM.jpg) ([View Tweet](https://twitter.com/mhevery/status/1628249291209994241))
	- To test() if a KEY is present
	  
	  bits[hash(KEY)%bits.length]
	  
	  If a bit present, it could be our KEY, OR it could be a collision. So we are not sure.
	  If a bit is NOT present, then we are 100% sure that KEY can not be there. 
	  
	  ![](https://pbs.twimg.com/media/Fpi0Gx8aQAAH6e2.jpg) ([View Tweet](https://twitter.com/mhevery/status/1628249301892857856))
	- To improve false positives
	- https://t.co/ZBQ6zbIVLD ([View Tweet](https://twitter.com/mhevery/status/1628249316325482496))
	- Hey, I am Miško, CTO at @builderio.
	  
	  We make a headless CMS that lets you drag-and-drop with your components, directly within your existing sites and apps.
	  
	  It makes for a much simpler codebase and workflow: https://t.co/DhG0Z7zax9 ([View Tweet](https://twitter.com/mhevery/status/1628249341814280192))