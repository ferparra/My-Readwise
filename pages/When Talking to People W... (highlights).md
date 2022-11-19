title:: When Talking to People W... (highlights)
author:: [[@chipro on Twitter]]
full-title:: "When Talking to People W..."
category:: #tweets
url:: https://twitter.com/chipro/status/1310952120431063041

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- 1. Deploying ML models is hard
	  
	  Deploying a model for friends to play with is easy. Export trained model, create an endpoint, build a simple app. 30 mins.
	  
	  Deploying it reliably is hard. Serving 1000s of requests with ms latency is hard. Keeping it up all the time is hard.
	  
	  (2/6)
		- **Tags**: #[[favorite]]
	- 2. You only have a few ML models in production
	  
	  Booking, eBay have 100s models in prod. Google has 10000s. An app has multiple features, each might have one or multiple models for different data slices.
	  
	  You can also serve combos of several models outputs like an ensemble.
	  
	  (3/6)
		- **Tags**: #[[favorite]]
	- 3. If nothing happens, model performance remains the same
	  
	  ML models perform best right after training. In prod, ML systems degrade quickly bc of concept drift.
	  
	  Tip: train models on data generated 6 months ago & test on current data to see how much worse they get.
	  
	  (4/6)
		- **Tags**: #[[statistical learning]] #[[favorite]]
	- 4. You won’t need to update your models as much
	  
	  One mindboggling fact about DevOps: Etsy deploys 50 times/day. Netflix 1000s times/day. AWS every 11.7 seconds.
	  
	  MLOps isn’t an exemption. For online ML systems, you want to update them as fast as humanly possible.
	  
	  (5/6)
	- Deploying ML systems isn't just about getting ML systems to the end-users.
	  
	  It's about building an infrastructure so the team can be quickly alerted when something goes wrong, figure out what went wrong, test in production, roll-out/rollback updates.
	  
	  It's fun!
	  
	  (6/6)