title:: EIP 1559 Is Even Better... (highlights)
author:: [[@barnabemonnot on Twitter]]
full-title:: "EIP 1559 Is Even Better..."
category:: #tweets
url:: https://twitter.com/barnabemonnot/status/1398105374587162625

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- EIP 1559 is even better than you think: it’s not quite true that whenever basefee is too low, we are back to how things are today (the first-price auction model) ([View Tweet](https://twitter.com/barnabemonnot/status/1398105362830544897))
		- **Note**: Thread
	- Today we rely on oracles to tell us the correct price. But oracles are reflexive! They are designed to parrot past prices back to current participants, and can perpetuate bubbles for longer than necessary ([View Tweet](https://twitter.com/barnabemonnot/status/1398105364424314882))
	- Under 1559, basefee is an *objective* measure of congestion, which catches up quickly to the true equilibrium price, bursting bubbles sooner, which means bidding wars are necessarily short-lived ([View Tweet](https://twitter.com/barnabemonnot/status/1398105366051778569))
	- Meanwhile, some of the block slack can absorb small demand shifts on its own, improving inclusion guarantees in slowly increasing demand conditions 
	  
	  ![](https://pbs.twimg.com/media/E2cP8O4VoAE1q7a.jpg) ([View Tweet](https://twitter.com/barnabemonnot/status/1398105371990921219))
	- This rings true! And we’ll also see ripple effects from having an in-protocol oracle for current network conditions, eg, for rollups to price the cost of publishing data to L1 and tune withdrawal period lengths https://t.co/vRCP1iB2Fb ([View Tweet](https://twitter.com/barnabemonnot/status/1398105374587162625))