title:: We Present Adaptive Skil... (highlights)
author:: [[@naokiyokoyama0 on Twitter]]
full-title:: "We Present Adaptive Skil..."
category:: #tweets
url:: https://twitter.com/naokiyokoyama0/status/1641805360011923457

- Highlights first synced by [[Readwise]] [[Apr 2nd, 2023]]
	- We present Adaptive Skill Coordination (ASC), an approach for robots to learn multi-skill tasks. Here is ASC deployed on Spot tidying up a house — navigating to a table/counter, finding and picking an object, and placing it elsewhere, repeating — with near-perfect performance!
	  🧵 https://t.co/StM60bxJq5 ([View Tweet](https://twitter.com/naokiyokoyama0/status/1641805360011923457))
		- **Note**: Thread
	- The robot is tasked to navigate to a receptacle located at a given goal coordinate, search for a target object, and pick it. It must then navigate to the object's target place receptacle, located at another goal coordinate, and place the object on it. 
	  
	  ![](https://pbs.twimg.com/media/Fsjb4hfWcAAiqnX.jpg) ([View Tweet](https://twitter.com/naokiyokoyama0/status/1641805364273336321))
	- ASC consists of 3 components:
	  1. a library of basic visuomotor skills (navigation, pick, place)
	  2. a skill coordination policy that chooses which skills are appropriate to use when
	  3. a corrective policy that adapts pre-trained skills when out-of-distribution states are perceived https://t.co/3PSKdZi8Sx ([View Tweet](https://twitter.com/naokiyokoyama0/status/1641805367242784768))
	- The coordination policy selects which skills to use for the current time step, while the corrective policy suggests alternative actions (i.e,. not from an expert) that can also be selected instead. 
	  
	  ![](https://pbs.twimg.com/media/FsjcL-DWcAAZ88n.jpg) ([View Tweet](https://twitter.com/naokiyokoyama0/status/1641805370749333505))
	- To adapt to the full task, the corrective policy learns behaviors out-of-distribution from those learned by basic skills. For example, while the navigation skill avoids approaching an obstacle, the corrective policy can instead go TOWARDS the obstacle to pick an object on it. https://t.co/W52VhEspHS ([View Tweet](https://twitter.com/naokiyokoyama0/status/1641805372796092416))
	- ASC performs better than a sequential skill-chaining baseline (98% vs. 73%), and demonstrates emergence of intelligent behavior such as faster skill hand-off; here, ASC switches to picking once the object is seen instead of waiting until the navigation goal is fully reached. https://t.co/FZVyiYhpEu ([View Tweet](https://twitter.com/naokiyokoyama0/status/1641805376998735873))
	- Though ASC was not trained to handle adversarial perturbations, it is robust to them at test-time: https://t.co/XHAOXXGnsL ([View Tweet](https://twitter.com/naokiyokoyama0/status/1641805380756938754))
	- For navigation, ASC is given the goal coordinate, and only observes the locations of obstacles through its depth camera. Because it’s trained to operate without maps, ASC can overcome changes in its environment, and navigates around active adversarial blocking as well. https://t.co/6ovL949ek8 ([View Tweet](https://twitter.com/naokiyokoyama0/status/1641805385085464578))
	- We hope that this project helps to demonstrate the strength of sim-to-real robot learning. Work done with Alex Clegg, Eric Undersander, @sehoonha, @DhruvBatraDB, and Akshara Rai. More info at https://t.co/ZiY3UfgF7C ([View Tweet](https://twitter.com/naokiyokoyama0/status/1641805389506150408))