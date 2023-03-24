title:: Episode 20 —  Hattie Zhou, Mila, on Supermasks, Iterative Learning, and Fortuitous Forgetting (highlights)
author:: [[Generally Intelligent]]
full-title:: "Episode 20 —  Hattie Zhou, Mila, on Supermasks, Iterative Learning, and Fortuitous Forgetting"
category:: #podcasts
url:: https://share.snipd.com/episode/2eb32f4b-97f4-4388-8685-b3692d362b8b

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- The Lottery Ticket Hypothesis for Deep Learning
	  
	  Summary:
	  The lottery ticket hypothesis presented a very interesting idea to me, which is that one of the reasons or part of the reason why over-parameterization is so helpful. The way they find these lottery tickets in the original paper by Jonathan Franco and Michael Carbon is by doing magnitude pruning. In fact, I think that even showed that you can do better than the original network by training the sparse network, which is pretty counterintuitive.
	  
	  Transcript:
	  Speaker 1
	  The lottery ticket hypothesis presented a very interesting idea to me, which is that one of the reasons or part of the reason why over-parameterization is so helpful is because when you initialize the model with a lot of weights, then just by random chance, you might get a subnetwork within that model that just is initialized at a good spot where it's easy for the model to learn the particular task. So if you have used lucky subnetworks, then the model could just leverage that good initial spot and go down a pretty nice path of learning. And when you have a lot of ways, then you have more chances, more combinations of these subnetworks, which is why they're called lottery tickets. So that was really intuitively appealing explanation for why over-parameterization is helpful. And the way they find these lottery tickets in the original paper by Jonathan Franco and Michael Carbon is by doing magnitude pruning. So you start with the normal network, you train it fully to your conversions, and then at the end of training, you look at which weights had the smallest magnitudes, and then for these weights, you prune them, meaning you set them to zero and you freeze them. And then for the remaining weights, you rewind them back to their initializations. And so these remaining weights would constitute the lottery ticket, essentially, the lucky subnetwork. And the paper showed that all you need to do to get to that performance of the original model is by training the subnetwork that you find.
	  
	  Speaker 2
	  In fact, I think that even showed that you can do better than the original network by training the sparse network, which is pretty counterintuitive. ([Time 0:08:59](https://share.snipd.com/snip/9f9472e1-89d3-4fe9-990e-7f138cf06510))
- New highlights added [[Mar 17th, 2023]] at 5:05 PM
	- What Is a Not-Correlational?
	  
	  Key takeaways: