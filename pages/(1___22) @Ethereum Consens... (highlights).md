title:: (1/22) @Ethereum Consens... (highlights)
author:: [[@SalomonCrypto on Twitter]]
full-title:: "(1/22) @Ethereum Consens..."
category:: #tweets
url:: https://twitter.com/SalomonCrypto/status/1576721911265996800

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- (1/22) @ethereum Consensus: Casper FFG
	  
	  The World Computer coordinates via Proof of Stake; validators place $ETH at stake in order to participate in the system. But what actually IS this system and how does it achieve consensus?
	  
	  A guide to Ethereum finality. 
	  
	  ![](https://pbs.twimg.com/media/FeGkN0QUUAAEvHQ.jpg) ([View Tweet](https://twitter.com/SalomonCrypto/status/1576721911265996800))
		- **Note**: Thread
	- (2/22) @ethereum exists between a network of 1,000s of computers, each running a local version of the Ethereum Virtual Machine (EVM).
	  
	  All copies of the EVM are kept perfectly in sync. Any individual EVM is a window into the shared state of the World Computer. https://t.co/oXdJCUqt4m ([View Tweet](https://twitter.com/SalomonCrypto/status/1576721916479488000))
	- (3/22) The EVM stays in sync through a process called consensus. A consensus mechanism is the system a blockchain uses to keep all its nodes in sync.
	  
	  Until recently, Ethereum used Proof of Work (PoW); ~2 weeks ago we experienced The Merge and switched to Proof of Stake (PoS). ([View Tweet](https://twitter.com/SalomonCrypto/status/1576721919176454144))
	- (4/22) Both PoW and PoS are systems that designate a "leader" node (validator) and allow them to progress their copy of the EVM forward (using transactions submitted from users like you and me).
	  
	  Once they have done as many transactions as they can, they create a block. ([View Tweet](https://twitter.com/SalomonCrypto/status/1576721921705594881))
	- (5/22) A block is a complete record of all the transactions that occurred within the EVM during each node's turn at being leader.
	  
	  Any other node can read the block, process the transactions and progress their copy of the EVM to match the leader. https://t.co/lliC9vVTkt ([View Tweet](https://twitter.com/SalomonCrypto/status/1576721924255756288))
	- (6/22) During normal operation, every ~12 seconds a leader is chosen, who then builds and proposes a block.
	  
	  However, the network can fall out of sync and more than one node might broadcast a validly produced block. 
	  
	  ![](https://pbs.twimg.com/media/FeGkPONUcAAX0Ig.jpg) ([View Tweet](https://twitter.com/SalomonCrypto/status/1576721932262600704))
	- (7/22) One of these choices is called a fork, and forks can grow.
	  
	  Even small forks are existential threats to a distributed system. Without one true blockchain, the independent EVMs on each node must decide which txns to execute. ([View Tweet](https://twitter.com/SalomonCrypto/status/1576721935567704066))
	- (8/22) This creates an issue for both the nodes of the network and the users of the network:
	  
	  The nodes can't be certain which is the one true path through the block tree.
	  
	  The users can't be certain if their txns are on the "true" path; if they aren't they wont count. ([View Tweet](https://twitter.com/SalomonCrypto/status/1576721938138877953))
	- (9/22) Casper the Friendly Finality Gadget (FFG) was introduced by @VitalikButerin and Virgil Griffith in 2019 to provide block certainty.
	  
	  BTW, all of you should know who Virgil Griffith is; he is paying for his belief in @ethereum.
	  
	  https://t.co/pfzSCdlquN ([View Tweet](https://twitter.com/SalomonCrypto/status/1576721940680581120))
	- (10/22) Casper FFG is a process that exists atop a block proposal mechanism; it is responsible for finalizing these blocks, canonizing the true @ethereum blockchain.
	  
	  Casper consists of two main parts: the finalization algorithm and the penalization scheme. ([View Tweet](https://twitter.com/SalomonCrypto/status/1576721943314632705))
	- (11/22) The finalization algorithm draws from the field of research derived from the Byzantine Generals Problem.
	  
	  The field looks for answers to the question "how can members of a network agree on a specific reality when no one can verify the identities of other members?" https://t.co/fFgO1JVSEe ([View Tweet](https://twitter.com/SalomonCrypto/status/1576721945852116992))
	- (12/22) Casper is derived from a particular solution to the Byzantine Generals Problem called practical Byzantine Fault Tolerance (pBFT).
	  
	  pBFT is a two vote process. After both votes, consensus can always be reached (as long as >2/3 of the validators are honest). https://t.co/uoe4m9HHG3 ([View Tweet](https://twitter.com/SalomonCrypto/status/1576721948586823681))
	- (13/22) At its core, pBFT uses a voting scheme to provide mathematical certainty that a decentralized network has made a collective, final decision.
	  
	  This is the principle that Casper applies: finalization certainty for @ethereum. ([View Tweet](https://twitter.com/SalomonCrypto/status/1576721951602708481))
	- (14/22) Rather than finalizing blocks, Casper finalizes "checkpoints," a single block once every N blocks (N = 32 blocks for PoS).
	  
	  The Casper equivalent of pBFT's voting is called a "supermajority link," meaning >2/3s of validators confirmed the validity of the checkpoint. 
	  
	  ![](https://pbs.twimg.com/media/FeGkQ9aUAAIylPr.jpg) ([View Tweet](https://twitter.com/SalomonCrypto/status/1576721961639550976))
	- (15/22) The two rounds of voting in pBFT are called prepare and commit; at the end of commit the action is final.
	  
	  In Casper, these ideas have different names: if a checkpoint has been confirmed once it is "justified." If it has been confirmed twice it is "finalized." ([View Tweet](https://twitter.com/SalomonCrypto/status/1576721965028503552))
	- (16/22) Every time a checkpoint is reached, each validator is responsible for evaluating the block and creating a vote.
	  
	  A vote simply marks the source checkpoint, the target block, proof of validity and the validator's signature. 
	  
	  ![](https://pbs.twimg.com/media/FeGkRlnUYAAZ8K5.jpg) ([View Tweet](https://twitter.com/SalomonCrypto/status/1576721972792152065))
	- (17/22) These votes are both a privilege and a responsibility of being a validator.
	  
	  Successfully voting earns $ETH rewards, but missing votes will incur an $ETH penalty.
	  
	  Voting maliciously will incur a much bigger penalty and get the validator removed from the network. 
	  
	  ![](https://pbs.twimg.com/media/FeGkSEOUcAA91-R.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FeGkSWVUYAIEHcP.png) ([View Tweet](https://twitter.com/SalomonCrypto/status/1576721986620821504))
	- (18/22) Building on the pBFT and the other research around the Byzantine Generals Problem, we can mathematically prove that these properties round out a robust BFT system.
	  
	  This thread is long enough, but the proofs are in the original Casper paper (tweet 9). ([View Tweet](https://twitter.com/SalomonCrypto/status/1576721991184265217))
	- (19/22) BFT systems have two properties: safety (any txn run by one node will be run by all) and liveness (consensus cannot stall).
	  
	  Casper FFG is not a full BFT algorithm (hence "gadget"). It will guarantee safety, but liveness depends on the proposal mechanism. ([View Tweet](https://twitter.com/SalomonCrypto/status/1576721993654620160))
	- (20/22) However, Casper does provide new properties:
	- (21/22) Casper FFG is a Proof of Stake system derived from decades of research - however it is not entirely complete.
	  
	  For one, there is no block proposal method. For another, Casper does not direct validators which checkpoint to pick if it needs to make a choice. ([View Tweet](https://twitter.com/SalomonCrypto/status/1576721998717235200))
	- (22/22) Fortunately, research did not stop in 2019; in fact, it still continues to this day, building on the work of pBFT and Casper.
	  
	  And before long, Casper will become mature enough to take center stake, Merge with LMD-GHOST and provide consensus to  @ethereum. ([View Tweet](https://twitter.com/SalomonCrypto/status/1576722001246695424))
	- Like what you read? Help me spread the word by retweeting the thread (linked below).  
	  
	  Follow me for more explainers and as much alpha as I can possibly serve. 
	  
	  https://t.co/vQbd2QxlnK ([View Tweet](https://twitter.com/SalomonCrypto/status/1576722163133923328))