title:: (1/21) Byzantine Fault T... (highlights)
author:: [[@SalomonCrypto on Twitter]]
full-title:: "(1/21) Byzantine Fault T..."
category:: #tweets
url:: https://twitter.com/SalomonCrypto/status/1576284739392090112

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- (1/21) Byzantine Fault Tolerance (BFT) and the Practical Solution (pBFT)
	  
	  What is the Byzantine Generals Problem? Why is it important for distributed systems? Does this problem have a solution?
	  
	  A guide to the core principles underlying decentralized consensus. 
	  
	  ![](https://pbs.twimg.com/media/FeAWnZrUYAA_EGv.jpg) ([View Tweet](https://twitter.com/SalomonCrypto/status/1576284739392090112))
		- **Note**: Thread
	- (2/21) The Byzantine Generals Problem was introduced by an academic paper in 1982. It describes a [[Game Theory]] problem that shows how difficult it can be for dispersed parties to reach an agreement (consensus) without help of a trusted central party.
	  
	  https://t.co/bqqu9IUFve ([View Tweet](https://twitter.com/SalomonCrypto/status/1576284742785191937))
	- (3/21) The Byzantine Generals Problem is a thought experiment: imagine an ancient city at war with Byzantium.
	  
	  The city is approached from all sides by 4 division of the Byzantine army. Each division has a general with unitary control over their division. 
	  
	  ![](https://pbs.twimg.com/media/FeAWn8HUcAALHBu.jpg) ([View Tweet](https://twitter.com/SalomonCrypto/status/1576284749932285953))
	- (4/21) The city is well defended; it will require the entire Byzantine army to capture it. If a single division (or a subset) attack, they will surely be defeated.
	  
	  After the generals arrive and make camp for the night, they must make a choice: tomorrow, will I fight or retreat? ([View Tweet](https://twitter.com/SalomonCrypto/status/1576284753204236288))
	- (5/21) Retreat entails an orderly withdrawal of your troops; it DOES NOT mean defeat.
	  
	  Defeat is attacking the city and losing the fight. Or letting your fellow general attack (and lose) while you retreat.
	  
	  All that matters is the generals act in unison. 
	  
	  ![](https://pbs.twimg.com/media/FeAWoh6VIAAa2xf.jpg) ([View Tweet](https://twitter.com/SalomonCrypto/status/1576284759847620609))
	- (6/21) Because this is ancient times, the generals have limited communication capabilities. All they can do is write a message on a piece of paper, give it to a messenger and send them to another general.
	  
	  Communication is asynchronous, bidirectional and uncoordinated. ([View Tweet](https://twitter.com/SalomonCrypto/status/1576284762838220801))
	- (7/21) In a perfect world, we could devise a relatively simple scheme. Maybe one general is elected a leader and sends out orders. Or maybe each general ranks their choices and the choice with the most votes wins...
	  
	  ...but this isn't a perfect world. ([View Tweet](https://twitter.com/SalomonCrypto/status/1576284765413523458))
	- (8/21) Remember, the Byzantine army is attacking a city... full of people... people who presumably don't want to Byzantine army to win.
	  
	  And so, they can disrupt communications. ([View Tweet](https://twitter.com/SalomonCrypto/status/1576284767946829825))
	- (9/21) Imagine a world in which the people of the city keep a very close eye out for the messengers moving between generals.
	  
	  What if they are able to capture a messenger and stop the message?
	  
	  Or what if they capture the messenger and REPLACE the message? ([View Tweet](https://twitter.com/SalomonCrypto/status/1576284770413137921))
	- (10/21) Maybe the people of the city have seen this invasion coming for months and have been planning sabotage the entire time.
	  
	  What if they were able to turn one of the Byzantine generals? ([View Tweet](https://twitter.com/SalomonCrypto/status/1576284773000966146))
	- (11/21) This is the core of the Byzantine Generals Problem: how can members of a network agree on a specific reality when no one can verify the identities of other members? ([View Tweet](https://twitter.com/SalomonCrypto/status/1576284775551156224))
	- (12/21) A Byzantine Fault describes a system with components that may fail but does not provide clear, reliable data on whether the component has failed.
	  
	  A message being replaced by the city defenders or a traitorous general lying are examples of Byzantine faults. ([View Tweet](https://twitter.com/SalomonCrypto/status/1576284778030018562))
	- (13/21) A system that is Byzantine Fault Tolerant (BFT) is a system that is capable of resisting this class of failures (and attacks).
	  
	  The Byzantine Generals’ Problem has more than one possible solution; thus, there are many possible BFT systems. ([View Tweet](https://twitter.com/SalomonCrypto/status/1576284780546510849))
	- (14/21) BFT systems (generally) try to optimize for two properties:
	  
	  Safety - all honest participants can agree on the sequence of events and therefore have the same information
	  
	  Liveness - the system must be able to eventually come to consensus and progress forward ([View Tweet](https://twitter.com/SalomonCrypto/status/1576284783117996032))
	- (15/21) A huge breakthrough came in 1999 with the publication of "Practical Byzantine Fault Tolerance" (pBFT).
	  
	  pBFT is "practical" meaning that it works in asynchronous environments (like the thought experiment... or the Internet) and is relatively fast.
	  
	  https://t.co/UYByOoHXBc ([View Tweet](https://twitter.com/SalomonCrypto/status/1576284785596518400))
	- (16/21) The pBFT algorithm provides safety and liveness assuming at least 2/3 + 1 nodes are honest.
	  
	  No BFT system can support networks with more than 1/3 faulty nodes. This is a mathematical property: 
	  
	  ![](https://pbs.twimg.com/media/FeAWqfLVUAAAH6M.png) ([View Tweet](https://twitter.com/SalomonCrypto/status/1576284793263648768))
	- (17/21) pBFT is complicated enough that it deserves it own deep dive.
	  
	  For now, pBFT works in a series of rounds. First a leader is chosen who then broadcasts the action to the group. ([View Tweet](https://twitter.com/SalomonCrypto/status/1576284796371681281))
	- (18/21) This is the typical diagram you will see; IMO it's pretty inaccessible.
	  
	  Node 0 is the leader, who broadcasts the action to the rest of the group (pre-prepare).
	  
	  Then each member of the group broadcasts its received message to all other members (prepare). 
	  
	  ![](https://pbs.twimg.com/media/FeAWrADUUAA4kOa.jpg) ([View Tweet](https://twitter.com/SalomonCrypto/status/1576284802038124546))
	- (19/21) Once each member has received the prepare messages, they then actually do the action. Finally, they broadcast confirmation that they did the action (commit).
	  
	  It is this two round system that gives pBFT its Byzantine fault-tolerance. ([View Tweet](https://twitter.com/SalomonCrypto/status/1576284804923867137))
	- (20/21) The original implementation also accounted for a faulty leader, however the process for detecting/replacing the leader (known as a "view change") was not scalable
	  
	  Nevertheless, its contribution is incalculable. In fact, it still lies at the basis of (most) Proof of Stake ([View Tweet](https://twitter.com/SalomonCrypto/status/1576284807448797184))
	- (21/21) Just remember... the Byzantine Generals Problems has many solutions. Those that look like pBFT are only one category of BFT systems
	  
	  Others look very different. Some might discard voting entirely. For example, maybe use some other type of work...
	  
	  https://t.co/ahY6OKJN0W ([View Tweet](https://twitter.com/SalomonCrypto/status/1576284809994739712))
	- Like what you read? Help me spread the word by retweeting the thread (linked below).  
	  
	  Follow me for more explainers and as much alpha as I can possibly serve. 
	  
	  https://t.co/fFgO1JVSEe ([View Tweet](https://twitter.com/SalomonCrypto/status/1576285014550990848))