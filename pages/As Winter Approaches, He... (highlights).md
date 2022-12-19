title:: As Winter Approaches, He... (highlights)
author:: [[@tessalau on Twitter]]
full-title:: "As Winter Approaches, He..."
category:: #tweets
url:: https://twitter.com/tessalau/status/1604018884662951938

- Highlights first synced by [[Readwise]] [[Dec 18th, 2022]]
	- As winter approaches, here's a story about why hardware is hard. ❄️🥶
	  
	  About a year ago, we started getting reports from the field about undesirable behavior when our robots were turned on. They would behave unpredictably. ([View Tweet](https://twitter.com/tessalau/status/1604018884662951938))
		- **Note**: Thread
	- Our engineering and CS team investigated all such reports to try to discover the root cause. Every time a report came in from the field, we'd immediately troubleshoot. We'd bring the robot back in house to try to replicate the failure. ([View Tweet](https://twitter.com/tessalau/status/1604018885833134086))
	- We couldn't reproduce it, but we did come up with a theory for why it was happening. It was the coupler that connected the motor to the wheel. If this came loose, the wheel wouldn't turn when it should and the robot would drive unpredictably. ([View Tweet](https://twitter.com/tessalau/status/1604018887603138561))
	- So we redesigned the coupler system so that it wouldn't slip under normal operation, and rolled out the fix to all robots. With many in customer hands, it took a while to cycle through them all. ([View Tweet](https://twitter.com/tessalau/status/1604018889460879360))
	- We also developed a field fix that involved taking the robot apart and tightening the coupler. The next time a customer called in with this problem, we had them apply this fix. And it worked! Problem solved. ([View Tweet](https://twitter.com/tessalau/status/1604018891461521408))
	- Fast forward to 2022. Last month, we started getting reports again of robots behaving erratically in the field. Again we brought the robots back in house, again we couldn't reproduce the behavior. ([View Tweet](https://twitter.com/tessalau/status/1604018893156388866))
	- This must be a new problem, we thought. After all, we had fixed the couplers and hadn't had any coupler-related issues for the past nine months. Our team started systematically debugging all other possible causes. ([View Tweet](https://twitter.com/tessalau/status/1604018894884130817))
	- We assigned an intern to try to reproduce the problem. Since it seemed to happen first thing in the morning, maybe it was related to the power-up sequence. The intern turned off and on a robot hundreds of times. It never showed the problem. ([View Tweet](https://twitter.com/tessalau/status/1604018896515715072))
	- Then someone had the brilliant idea to put a robot in the fridge. We pulled it out the next morning, and ... it exhibited the problem. For ten minutes. Then it stopped. Could it have something to do with temperature? ([View Tweet](https://twitter.com/tessalau/status/1604018898172489728))
	- Ten minutes didn't give us a lot of time to debug before the problem went away. So we filled the fridge with robots, and took them out one by one to experiment on. The kitchen became an OR, with robot cadavers spread out on operating tables. 
	  
	  ![](https://pbs.twimg.com/media/FkKesZLUUAA2yLz.jpg) ([View Tweet](https://twitter.com/tessalau/status/1604018904606470144))
	- Some of the experiments involved measuring what was happening inside the bot while it was cold. At one point I found a scope outside the fridge, measuring the vitals of the patient inside. 
	  
	  ![](https://pbs.twimg.com/media/FkKesxXUUAAlKE3.jpg) ([View Tweet](https://twitter.com/tessalau/status/1604018911963361281))
	- Finally we discovered the problem. One of the off-the-shelf components we use behaved out of spec at certain temperatures, generating a noisy signal. We reverse engineered the component and found that removing two resistors fixed it. Problem solved, for real this time. ([View Tweet](https://twitter.com/tessalau/status/1604018914433765376))
	- Turns out that last year's coupler problems had the same root cause. While people were opening up the robot and tightening the coupler, the robot would warm up. By the time they put it back together, the problem would have gone away. It had nothing to do with couplers at all. ([View Tweet](https://twitter.com/tessalau/status/1604018916522876928))
	- By the time we had rolled out the coupler "fix" to all robots, the weather had warmed up enough across the country that the issue didn't reoccur. We thought we had fixed it, when actually spring fixed it. ([View Tweet](https://twitter.com/tessalau/status/1604018918557089792))
	- When you realize that there are hundreds of components in the simplest robot, and each one can have unpredictable failure modes like this one ... that's why hardware is hard. Kudos to Team Dusty for solving hard problems like these! ([View Tweet](https://twitter.com/tessalau/status/1604018920385495041))
	- If this sounds like fun, we're hiring! https://t.co/NQM5r5XCm9 ([View Tweet](https://twitter.com/tessalau/status/1604018922339983360))