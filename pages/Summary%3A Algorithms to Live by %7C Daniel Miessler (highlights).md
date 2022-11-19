title:: Summary: Algorithms to Live by | Daniel Miessler (highlights)
author:: [[danielmiessler.com]]
full-title:: "Summary: Algorithms to Live by | Daniel Miessler"
category:: #articles
url:: https://danielmiessler.com/projects/reading/summary-algorithms-to-live-by/

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- The Secretary Problem is a form of the Optimum Stopping problem, where you’re not sure when you should stop searching for an optimum form of something. You could keep searching and maybe find something better, but that might be a waste of time you should be spending on something else. There is an actual answer: which is 37%. Optimum Stopping is about avoiding stopping too early or too late. If you follow this optimal strategy you will also have a 37% chance of finding the best thing.
	- This is also related to the look-then-leap rule, which is where you spend a certain amount of time looking and not choosing anyone, and then after that point you pick the very first person that’s better than everyone you’ve seen so far.
	- a slower mind in old age could simply be a search problem, because the database is exponentially larger than when you’re 20.
	- The optimal strategy for that goal is a simple modification of Shortest Processing Time: divide the weight of each task by how long it will take to finish, and then work in order from the highest resulting importance-per-unit-time (call it “density” if you like, to continue the weight metaphor) to the lowest.
	- It turns out, though, that even if you don’t know when tasks will begin, Earliest Due Date and Shortest Processing Time are still optimal strategies, able to guarantee you (on average) the best possible performance in the face of uncertainty.
	- Laplace’s Law, and it is easy to apply in any situation where you need to assess the chances of an event based on its history. If you make ten attempts at something and five of them succeed, Laplace’s Law estimates your overall chances to be 6/12 or 50%, consistent with our intuitions. If you try only once and it works out, Laplace’s estimate of 2/3 is both more reasonable than assuming you’ll win every time, and more actionable than Price’s guidance (which would tell us that there is a 75% metaprobability of a 50% or greater chance of success).
	- The Copernican Principle says that if you want to estimate how long something will go on, look at how long it’s been alive, and add that amount of time
	- there are two types of things in the world: things that tend toward (or cluster around) some kind of “natural” value, and things that don’t.
	- whether it’s having incomplete information when interviewing job applicants, dealing with a changing world when trying to resolve the explore/exploit dilemma, or having certain tasks depend on others when we’re trying to get things done—the more likely we are to end up in a situation where finding the perfect solution takes unreasonably long