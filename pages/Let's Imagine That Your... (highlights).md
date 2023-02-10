title:: Let's Imagine That Your... (highlights)
author:: [[@crichardson on Twitter]]
full-title:: "Let's Imagine That Your..."
category:: #tweets
url:: https://twitter.com/crichardson/status/1622996667510169600

- Highlights first synced by [[Readwise]] [[Feb 9th, 2023]]
	- Let's imagine that your developing a microservices-based application and you need to implement a major new feature. For example, you want to implement coupons: 
	  
	  ![](https://pbs.twimg.com/media/FoYK3fTXoAAJr9p.png) ([View Tweet](https://twitter.com/crichardson/status/1622996667510169600))
		- **Note**: Thread
	- The Coupon Management subdomain needs to be part of a service.
	  But which service?
	  You might automatically implement Coupon Management as a new Coupon Service.
	  After all your application has a MICROservice architecture, which means lots of services, right? ([View Tweet](https://twitter.com/crichardson/status/1622996669775155201))
	- The trouble, however, with blindly adding new services, is that it often leads to the More the Merrier anti-pattern: an overly complex architecture that's difficult to maintain and, perhaps, brittle.
	  
	  https://t.co/tOIZ4rGrb0 
	  
	  ![](https://pbs.twimg.com/media/FoYK39xXsAYU9J_.jpg) ([View Tweet](https://twitter.com/crichardson/status/1622996675739496455))
	- Rather than blindly adding new services, a much better approach is brainstorm various possible designs and evaluate them using the dark energy and dark matter forces: 
	  
	  https://t.co/9dh4FwyYqF 
	  
	  ![](https://pbs.twimg.com/media/FoYK4W9XsAoLMkm.jpg) ([View Tweet](https://twitter.com/crichardson/status/1622996682337136643))
	- For example, there are three possible ways to implement Coupon Management:
	  
	  * Separate Coupon Service
	  * As part of the Order Service
	  * As part of the Customer Service
	  
	  Each of these three options has different trade-offs with respect to the dark energy and dark matter forces. ([View Tweet](https://twitter.com/crichardson/status/1622996684773945351))
	- To find out the details please read this article and recent presentation that I gave at the Melbourne Platform Engineering meetup.
	  
	  https://t.co/PEsTUQPgYm 
	  
	  ![](https://pbs.twimg.com/media/FoYK44QXEAAXDTp.jpg) ([View Tweet](https://twitter.com/crichardson/status/1622996692864798731))
	- That's a wrap!
	  
	  If you enjoyed this thread:
	  
	  1. Follow me @crichardson for more of these
	  2. RT the tweet below to share this thread with your audience
	  3. Contact me about consulting and training ([View Tweet](https://twitter.com/crichardson/status/1622996695771492352))