title:: 1) I Talked With @Vitali... (highlights)
author:: [[@SBF_Alameda on Twitter]]
full-title:: "1) I Talked With @Vitali..."
category:: #tweets
url:: https://twitter.com/SBF_Alameda/status/1343436567847739392

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- 2) NOT INVESTMENT ADVICE
	  
	  @VitalikButerin -- if I get your thoughts wrong here, definitely call me out on it!
	  
	  And also feel free to give more color.
	- 3) After our panel on effective altruism, Vitalik and I talked about a bunch of stuff; one topic was on different layer 1 blockchains.
	  
	  My main question was:
	  
	  What does he think makes an L1 better, or worse?
	- 4) And more specifically:
	  
	  What could @solana do that would make it better?
	  
	  This wasn't about Solana in an absolute sense; obviously Vitalik thinks Ethereum is better.
	  
	  This was about what it could do to be more good and less bad than it is now. 
	  
	  -------
	  
	  Some background:
	- 5) There are a lot of axes on which blockchains can differ!
	  
	  This will primarily focus on two:
	  
	  a) speed/throughput
	  b) security/consensus
	  
	  My argument: the main advantage of Solana is that it's really fast.
	  
	  Now, *all* geographically distributed chains have block times > 100ms.
	- 6) That's the time it takes light to go around the world, roughly.
	  
	  But Solana manages to get roughly 50,000 transactions through per second right now, with the ability to scale up to 1m or so.
	  
	  And all of those are on the same shard: they can all compose with each other.
	- 7) The main thing we compared it to was ETH 2.0, coming out over the next few years.
	  
	  ETH2 is closer to 1k TPS *per shard*, but can can have multiple shards.
	  
	  Each shard is independent on short timescales, synching up on longer ones.
	- 8) The cost of ETH2 is that you can't have a coherent, composing ecosystem that collectively takes > 1k TPS.
	  
	  A cypto exchange, Facebook, Twitter, WeChat, Alipay, etc. each take ~10k-10m TPS, so won't fit on a shard, or really on ETH2.
	  
	  --------
	- 9) But there are a lot of advantages to ETH2 over Solana.
	  
	  It will come with a larger built-in ecosystem, more active developers, more validators, more value securing the protocol, etc.
	  
	  The biggest thing that Vitalik pointed to, though, was the cost of running a node.
	- 10) This was probably the crux of it for him.
	  
	  You can run an ETH2 node on a laptop; Solana requires a decently high performance desktop.
	  
	  There are a lot of reasons this matters; one is that it's easier to debug something that's slower.
	  
	  But the largest is decentralization.
	- 11) On ETH2, it's plausible that there could be 10m validators and 1m block producers; 100m+ laptops are made each year.
	  
	  And more crucially, *most users of ETH2 could run a node for very little cost*.
	  
	  That means that a random person using an ETH2 DEX could validate its shard.
	- 12) This doesn't mean it can validate the whole blockchain--it likely couldn't--but it could validate the shard of the application it was using.
	  
	  This means that each user could practically verify themselves that the transactions they were doing were legit.
	- 13) This provides a huge added layer of security: even if consensus broke down and the block producers tried to do something nefarious, each user could notice and call bullshit.
	  
	  Even if they didn't have 51% stakeweight, if 80% of users disagree with a block, they can hard fork.
	- 14) How about Solana?
	  
	  Well, the cost of running a node is dedicating a ~$500 machine to it.
	  
	  Which isn't that much, for a large player in crypto!
	  
	  But it is for a random user.
	  
	  And so in practice only people fairly interested in the ecosystem are likely to run nodes.
	- 15) This doesn't necessarily effect literal consensus that much--those players likely had most of the stakeweight anyway, because anyone with large stakeweight could easily get a machine to validate.
	  
	  But it does mean that a random user might not be able to call bullshit.
	- 16) You lose the sense of each person, practically speaking, validating their own transactions.
	  
	  ----------
	  
	  Anyway, enough preamble.  What could make a high throughput chain relatively more secure?
	  
	  There were basically two types of suggestions Vitalik had.
	- 17) The first was variants on "find some sub-unit and split validation on it".
	  
	  This is what sharding does.
	  
	  Some examples that might work on Solana:
	  
	  a) One huge shard plus lots of small shards.  Basically, the 'main' shard would be what Solana is now.
	- 18) Smaller shards would limit themselves to ~1k TPS, and be designed so that a laptop could validate them.
	  
	  That way people really concerned with validating their own transactions could use smaller shards, and apps the require large usage or composability could use the large one
	- 19) b) Another ideas was to split the blockchain into "domains"; this could be e.g. addresses invoking calls, or tx number mod 20.  Make it so that each validator is assigned to a domain and can only produce blocks for that one.
	- 20) This means that, no matter how large a validator is, it can only ever produce blocks for e.g. 5% of the ecosystem.
	  
	  That forces further decentralization of block production, and means that you need to get a more diverse set of validators on board with a timeline.
	- 21) There were some other ideas whose details I've forgotten -- "big blocks/small blocks", "some small validator that has some power"-- @VitalikButerin do you remember those?
	  
	  --
	  
	  The other set of ideas were about storing state securely and efficiently.
	- 22) The goal here would be two-fold: make sure history can't be rewritten; and that it's easy for a low-powered validator to find out the state of the blockchain.
	  
	  One idea here is just writing the state to the ETH blockchain periodically.  Then any ETH node could verify Solana.
	- 23) Another idea was to write ZK-proofs of a Merkle tree of the blockchain, or something like that.
	  
	  A third thing that Vitalik brought up: it would be great if each block header contained the full state of the blockchain, so at least verifying that was easy for a laptop.
	- 24) I'm probably missing a lot of his thoughts here, and probably misrepresented some too--sorry!
	  
	  But I found the conversation super interesting.
	  
	  There are sometimes tradeoffs between security and speed, but at least we can try to find a pareto maxima.
	- 25) @VitalikButerin -- how did I do summarizing this?  What are your thoughts, in your words?
	  
	  @aeyakovenko -- thoughts on the above?