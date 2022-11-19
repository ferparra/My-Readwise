title:: (1/20) @Ethereum Fundame... (highlights)
author:: [[@SalomonCrypto on Twitter]]
full-title:: "(1/20) @Ethereum Fundame..."
category:: #tweets
url:: https://twitter.com/SalomonCrypto/status/1578540111930699778

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- (1/20) @ethereum Fundamentals: Attestation
	  
	  Ethereum is made up of 1000s of computers, each contributing to its security by providing their Proof of Stake. But how does it actually work? How do 1000s of computers participate? What are they doing?
	  
	  A guide to voting with $ETH. 
	  
	  ![](https://pbs.twimg.com/media/FegZ3YCUcAADeWr.jpg) ([View Tweet](https://twitter.com/SalomonCrypto/status/1578540111930699778))
		- **Note**: Thread
	- (2/20) @ethereum is the World Computer, a globally shared platform that exists between a network of 1,000s of computers, each running a local copy of the Ethereum Virtual Machine (EVM).
	  
	  Every local EVM is in sync; the state of any node is the state of the World Computer. https://t.co/9kMC3tZOQx ([View Tweet](https://twitter.com/SalomonCrypto/status/1578540115063762945))
	- (3/20) This distributed network of EVMs is held in sync via a consensus mechanism.
	  
	  A consensus mechanism is a system by which a leader (block proposer) updates the state of their EVM and the rest of the network trustlessly follows. https://t.co/MNCgASO7Fj ([View Tweet](https://twitter.com/SalomonCrypto/status/1578540117844631552))
	- (4/20) Today, @ethereum uses Proof of Stake (PoS).
	  
	  PoS randomly selects a block proposer, who gets to construct the next block. The rest of the network validates these blocks, voting them into the blockchain.
	  
	  In order to participate, you must put $ETH at stake. https://t.co/OYFYmYvPrm ([View Tweet](https://twitter.com/SalomonCrypto/status/1578540120596021248))
	- (5/20) By putting $ETH at stake, network participants (validators) are placing their capital at risk for slashing - the punishment the network applies to malfunctioning (intentional or not) validators.
	  
	  This is the mechanism by which the $ETH stake projects economic security. ([View Tweet](https://twitter.com/SalomonCrypto/status/1578540123402092544))
	- (6/20) Most obviously, this dynamic applies to the block proposer; if they submit an invalid block, the network will consider them a malicious actor and remove them from the network.
	  
	  But this also applies to the next step - the validation of the block by the rest of the network. ([View Tweet](https://twitter.com/SalomonCrypto/status/1578540126052835329))
	- (7/20) The block producer sends out a block; validators evaluate it and if it is valid, they broadcast an attestation.
	  
	  If a validator attests to an invalid block, the network considers them just as hostile as an invalid block proposer.
	  
	  Attestations are core to $ETH security. ([View Tweet](https://twitter.com/SalomonCrypto/status/1578540128640720896))
	- (8/20) Alright, we've finally made it. Now that we understand how attestations fit in to the World Computer, we can finally dig in: what is an attestation?
	  
	  It starts with a block, broadcast to the network. 
	  
	  ![](https://pbs.twimg.com/media/FegZ4omUAAEjNut.jpg) ([View Tweet](https://twitter.com/SalomonCrypto/status/1578540135418691584))
	- (9/20) Sending the block to a few (or even 1,000) validators is no problem, but once you start getting passed 10K, the chatter requirements become so huge that no credibly decentralized network could handle it.
	  
	  Currently there are about 440k @ethereum validators. 
	  
	  ![](https://pbs.twimg.com/media/FegZ5DzUYAAt64t.jpg) ([View Tweet](https://twitter.com/SalomonCrypto/status/1578540142783971328))
	- (10/20) An @ethereum where every validator validates every block is not realistic. Instead, we have a different goal: every validator will validate every epoch.
	  
	  One epoch = 32 blocks = 6.4 minutes.
	  
	  Once every 6.4 minutes every validator will vote on the canonical blockchain. https://t.co/rOsQpim0ic ([View Tweet](https://twitter.com/SalomonCrypto/status/1578540145917063168))
	- (11/20) At the beginning of every epoch (once every 32 blocks), the entire validator set is randomly shuffled into 32 groups called committees.
	  
	  The block proposer sends every validator a copy of the block, but only its committee members need to attest. 
	  
	  ![](https://pbs.twimg.com/media/FegZ5pfUUAMVvoZ.jpg) ([View Tweet](https://twitter.com/SalomonCrypto/status/1578540153034809344))
	- (12/20) Zooming in, an attestation is really a BLS signature wrapped in some identifying metadata
	  
	  A BLS signature is a type of digital signature that maintains all the properties of a normal digital signature but with a special property: multiple keys/messages can be aggregated https://t.co/YZuAed9p3X ([View Tweet](https://twitter.com/SalomonCrypto/status/1578540156130234368))
	- (13/20) The magic of BLS signatures is that at the data level, an aggregate signature is the exact same thing as a single signature.
	  
	  Thus, a BLS signature can store (and verify) a HUGE amount of signatures in a very efficient manner. https://t.co/G3WJe0oQ3j ([View Tweet](https://twitter.com/SalomonCrypto/status/1578540158797766656))
	- (14/20) If there are 440k validators and 32 committees, there must be ~14k validators/committee.
	  
	  14k validators still poses a problem; it's both too much network chatter and too many signatures to aggregate all at once.
	  
	  And so, we split one more time. 1 committee = 64 subnets. ([View Tweet](https://twitter.com/SalomonCrypto/status/1578540161628971008))
	- (15/20) Validators broadcast their attestations to their assigned subnet, which consist of ~250 validators.
	  
	  16 validators on each committee are designated as aggregators. They listen for attestations and begin bundling them into a BLS signature. 
	  
	  ![](https://pbs.twimg.com/media/FegZ6joVQAAHSdL.jpg) ([View Tweet](https://twitter.com/SalomonCrypto/status/1578540168855769088))
	- (16/20) All 16 are attempting to build the same aggregate signature containing all the subnet's validators, but network conditions can cause some aggregators to miss a few attestations. There's only so much you can do. 🤷‍♂️
	  
	  Each validator does their best and publishes the result. ([View Tweet](https://twitter.com/SalomonCrypto/status/1578540172018262016))
	- (17/20) At this point, the ball moves back to the block producer's court. The validator who proposed the node begins to go subnet by subnet and selects the best aggregate signature.
	  
	  Once the 64 best signatures are gathered, the block proposer aggregates them one last time. ([View Tweet](https://twitter.com/SalomonCrypto/status/1578540174601965571))
	- (18/20) This final aggregation is then added on to the block, signifying that all 14k validators in that committee saw that block and agreed with it - on threat of slashing.
	  
	  Incidentally this process limits the number of validators the network can support. https://t.co/PCk8ESVMAu ([View Tweet](https://twitter.com/SalomonCrypto/status/1578540177215041536))
	- (19/20) At this point we have a valid block, attested to by its entire committee and carefully prepared to allow quick verification. And so, it's time to add it to the blockchain...
	  
	  In fact, by virtue of this process, it WAS added to the blockchain. 
	  
	  ![](https://pbs.twimg.com/media/FegZ7eRVIAA1N9d.jpg) ([View Tweet](https://twitter.com/SalomonCrypto/status/1578540184089436161))
	- (20/20) Every time a block is proposed, 1/32 of the network places their stake on the line and votes.
	  
	  Every 32 blocks, the entire network participates.
	  
	  And so, once every epoch, @ethereum becomes secured by the entire value of all staked $ETH. ([View Tweet](https://twitter.com/SalomonCrypto/status/1578540187352588288))
	- Like what you read? Help me spread the word by retweeting the thread (linked below).  
	  
	  Follow me for more explainers and as much alpha as I can possibly serve. 
	  
	  https://t.co/KYICTCVGUb ([View Tweet](https://twitter.com/SalomonCrypto/status/1578540301408272386))