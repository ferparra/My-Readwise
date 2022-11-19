title:: Another Common Question... (highlights)
author:: [[@jmwind on Twitter]]
full-title:: "Another Common Question..."
category:: #tweets
url:: https://twitter.com/jmwind/status/1477399261700526080

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Another common question I’m answering working with scaling tech companies is…
	  
	  Q. What virus infects growing engineering orgs the most?
	  
	  A. Layerinitis. Let me explain... 🧵 (1/27) 
	  
	  ![](https://pbs.twimg.com/media/FIDGzJmVkAglUww.png) ([View Tweet](https://twitter.com/jmwind/status/1477399261700526080))
		- **Note**: Thread
	- 2/ As your eng org grows you have to organize into teams. Companies start with shared ownership of the code base and small project teams that form and disband. It's a good model, but past 50+ engineers that falls apart... ([View Tweet](https://twitter.com/jmwind/status/1477399263436939268))
	- 3/ In 2015 at Shopify there was a busy file called api_client.rb. I spoke to the last 20 committers. Everyone was adding new attributes, but when asked why the answer was "I was just following what the previous committer did" an "had a deadline". ([View Tweet](https://twitter.com/jmwind/status/1477399264661671938))
	- 4/ The design philosophy of that entire area of Shopify was shared across everyone. But there was no real owner or steward. As they say... the fastest way to starve a horse is to ask two people to feed it. ([View Tweet](https://twitter.com/jmwind/status/1477399265752190977))
	- 5/ So as you'd expect, as your org grows, you create teams that have stewardship for areas of your product. 
	  
	  There's a lot of research that shows that code ownership increases the quality of software. https://t.co/tnLBz90GRT ([View Tweet](https://twitter.com/jmwind/status/1477399266767167488))
	- 6/ At this point you think you've got everything figured out. You define boundaries in your software, modularity is good. You can reduce dependencies with good APIs, DDD, and increase the overall quality all at once. You're winning! That was easy... right? ([View Tweet](https://twitter.com/jmwind/status/1477399267950022657))
	- 7/ We modularized somewhat retroactively at Shopify (read about it https://t.co/QkI4V6UhuL) and we started with a modular architecture at https://t.co/nqinl4d0FA in 2000. ([View Tweet](https://twitter.com/jmwind/status/1477399269082497024))
	- 8/ But what you didn't realize is that layerinitis has been lurking just waiting to attack your org. It's triggered right at that moment when you think you have the perfect architecture and team structure. And it hits hard. ([View Tweet](https://twitter.com/jmwind/status/1477399270244294656))
	- 9/ You also likely have PMs matched up to each team and you want them to be as independent as possible. You want to stay fast and nimble and your incentives are aligned for that (promotions, raises)... ([View Tweet](https://twitter.com/jmwind/status/1477399271397756928))
	- 10/ Then you realize that 80% of the projects that introduce new features or capabilities look like this: 
	  
	  ![](https://pbs.twimg.com/media/FIDGz8OVcAMnZm8.jpg) ([View Tweet](https://twitter.com/jmwind/status/1477399275050967042))
	- 11/ But the code is always added at the top of your stack. This is a very human response by teams, you have incentives aligned to ship fast at the teams level and it's much easier to measure that vs if the code in the right spot for the long term health of your system. ([View Tweet](https://twitter.com/jmwind/status/1477399276384751616))
	- 12/ The technical definition for layerinitis is teams putting code where they are most comfortable while optimizing for speed vs putting the code where it belongs when considering a longer term perspective on the overall software system. ([View Tweet](https://twitter.com/jmwind/status/1477399277408194563))
	- 13/ It's very easy to diagnose, so that's great news. Ask teams where the code should go for their project if they break down the capabilities they are introducing with their project into the model introduced here: https://t.co/g2FyJresrp ([View Tweet](https://twitter.com/jmwind/status/1477399278519668737))
	- 14/ Let's pause a second. Layerinitis isn't bad, it's a virus that every org will get. We've all been there. But there are cultural, process, and tooling tricks you can implement that will prevent layerinitis from crippling your teams. ([View Tweet](https://twitter.com/jmwind/status/1477399279731838978))
	- 15/ Starting with culture, ask yourself, do teams have permission to learn and build confidence with different parts of your software stack? ([View Tweet](https://twitter.com/jmwind/status/1477399280851644418))
	- 16/ One memorable experience at Shopify was when we tried to add subscriptions to the platform for 2 years. The team who owned the featured owned the UI parts of the online store. So every solution ended up a very UI focused solution. ([View Tweet](https://twitter.com/jmwind/status/1477399281896067073))
	- 17/ I took the team into a boardroom, they were all extremely smart engineers. They were stressed. I changed the goals of the project: 1) your mission is to find the best place to build subscriptions into Shopify 2) build a prototype / fork any repo and we will throw it away. ([View Tweet](https://twitter.com/jmwind/status/1477399282940452868))
	- 18/ A big lesson from this is that the team had the skill to do the work, but never had permission to deeply build confidence in other areas of the code base. They didn't see their role as stewards of the overall architecture of Shopify vs shipping the feature. ([View Tweet](https://twitter.com/jmwind/status/1477399284047695872))
	- 19/ We often forget that prototyping isn't just about finding a good architecture or figuring out how long something will take to build. One of the most important benefits of prototypes is increasing the confidence in your engineering teams to work and understand layers. ([View Tweet](https://twitter.com/jmwind/status/1477399285217914880))
	- 20/ I've seen so many teams that replace prototypes with roadmaps. Then they stop building to learn. And now they have roadmaps with no substance. It's a vicious circle. ([View Tweet](https://twitter.com/jmwind/status/1477399286304296960))
	- 21/ There's another big side effect of using prototypes as a way to dampen layerinitis. Often the prototype team end of digging into platform / infra level areas that are often owned by small teams. Those teams really appreciate having more people learn about their areas... ([View Tweet](https://twitter.com/jmwind/status/1477399287399006208))
	- 22/ ...over time I've seen a healthy growth of morale and committers across different layers just by encouraging more cross-layer prototype at the start of large projects. And that builds more long term resiliency of knowledge across your teams. ([View Tweet](https://twitter.com/jmwind/status/1477399288460156931))
	- 23/ Once you have a few good cultural habits, the next change that helps is a process one. Ensure you have enough flexibility in your roadmaps to put people from across different layers of your stack onto the projects that need them... ([View Tweet](https://twitter.com/jmwind/status/1477399289596764168))
	- 24/ ...this may sound trivial, but every company has an army of people managing crazy gantt charts that will explode when re-jiggle people. But do it anyway. 
	  
	  You had one job as a manager... put the right skills on the right projects. Period. 
	  
	  ![](https://pbs.twimg.com/media/FIDG1BLVcAA-Ahu.png) ([View Tweet](https://twitter.com/jmwind/status/1477399294562820096))
	- 25/ The next layerinitis defence is standardizing access and setup of any code base in your company. You should have the same command to setup a dev environment, test, tools for every code base. ([View Tweet](https://twitter.com/jmwind/status/1477399296311844865))
	- 26/ You need amazing READMEs that assume that those reading are new and want to learn how to contribute vs just use. Again, sounds trivial but some many teams have crappy READMEs that make it hard and intimidating to setup and contribute. ([View Tweet](https://twitter.com/jmwind/status/1477399297381392384))
	- 27/ That's the short summary of why I think that layerinitis is the worst virus that will eventually infect your engineering org and the defences you can start to build now. 
	  
	  ![](https://pbs.twimg.com/media/FIDG1cTUYAAVMWs.png) ([View Tweet](https://twitter.com/jmwind/status/1477399300850159616))