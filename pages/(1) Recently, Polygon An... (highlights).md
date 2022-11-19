title:: (1) Recently, Polygon An... (highlights)
author:: [[@han_sungjae on Twitter]]
full-title:: "(1) Recently, Polygon An..."
category:: #tweets
url:: https://twitter.com/han_sungjae/status/1412039192037629954

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- (1) Recently, Polygon announced their new data availability layer named “Avail”, which brought some attention to this technology where originally a project named Celestia (previously LazyLedger) was working on. @CelestiaOrg @0xPolygon @Mustafa ([View Tweet](https://twitter.com/han_sungjae/status/1412039162744565766))
		- **Note**: Thread
	- (2) However, due to its complex nature, most people don't try to understand it. In this thread, I try to explain simply the whats and whys of a data availability infrastructure they’re building. First, let's understand the data availability problem. ([View Tweet](https://twitter.com/han_sungjae/status/1412039164153909248))
	- (3) Data availability problem occurs when a block producer publishes a block header that is valid but purposely obscures the underlying transaction data. This is a problem because light nodes only rely on the block header to verify and can be tricked into accepting invalid blocks ([View Tweet](https://twitter.com/han_sungjae/status/1412039165554806797))
	- (4) Full nodes can’t generate data availability proofs for light nodes that the block is missing data in the same way they can generate fraud proofs for invalid blocks. Light nodes have to verify the data availability itself or have an honest majority assumption. ([View Tweet](https://twitter.com/han_sungjae/status/1412039166905315331))
	- (5) This is why most nodes have to download tx data and verify the data availability of a block. This poses certain scalability limits and problems to different scaling solutions such as increasing block sizes, sharding, and rollups as the complexity of verification increases. ([View Tweet](https://twitter.com/han_sungjae/status/1412039168268460033))
	- (6) So how do Avail and Celestia tackle this problem? They build a blockchain where its consensus only verifies ordering and data availability without transaction execution/verification. ([View Tweet](https://twitter.com/han_sungjae/status/1412039169619021830))
	- (7) To fully understand this, let’s look at the general blockchain architecture first. The general blockchain architecture consists of the three following layers: The execution layer, the consensus layer, and the data availability layer. ([View Tweet](https://twitter.com/han_sungjae/status/1412039170910875655))
	- (8) For most blockchains like Ethereum, all three layers are coupled together in a monolithic architecture - Ethereum virtual machine is part of the consensus rules and the protocol. 
	  
	  ![](https://pbs.twimg.com/media/E5iQCk7VoAIv-PW.png) ([View Tweet](https://twitter.com/han_sungjae/status/1412039172244660227))
	- (9) Projects like Celestia and Avail provide a separate data availability layer and a consensus layer where different blockchains/execution environments can benefit from. ([View Tweet](https://twitter.com/han_sungjae/status/1412039174056661003))
	- (10) They work as a minimal, pluggable consensus and data availability layer that only verifies data availability and transactional ordering. This allows a modular architecture of a blockchain network which offers more flexibility. 
	  
	  ![](https://pbs.twimg.com/media/E5iQTLHVIAEb3Yu.png) ([View Tweet](https://twitter.com/han_sungjae/status/1412039175398854661))
	- (11) The separate data/consensus layer is very scalable because they use mathematical data availability proofs (Celestia uses erasure coding and Avail uses KZG commitment schemes) that perform DA checks very efficiently. ([View Tweet](https://twitter.com/han_sungjae/status/1412039177227567106))
	- (12) The execution consensus bottleneck is solved here by only performing data availability proofs without having to verify the state and validity of a block by execution. ([View Tweet](https://twitter.com/han_sungjae/status/1412039178557083651))
	- (13) The implication of the separate layer is that sovereign execution environments, especially application-specific blockchains, can plug into Avail or Celestia and benefit from its security without having to bootstrap its own validator set/consensus. ([View Tweet](https://twitter.com/han_sungjae/status/1412039179878289415))
	- (14) This will allow application-specific blockchain networks to scale and benefit from the security secured by the Celestia/Avail (The data availability and consensus layer) ([View Tweet](https://twitter.com/han_sungjae/status/1412039181220540422))
	- (15) However, because they do not verify the validity of the transactions, the execution has to be implemented in some ways to handle both execution and verification/dispute resolutions. ([View Tweet](https://twitter.com/han_sungjae/status/1412039182504005644))
	- (16) Celestia proposes optimistic rollups as a solution and has proposed to add rollup support to Cosmos SDK, but essentially, you can build any execution layer on top of the data/consensus layer. ([View Tweet](https://twitter.com/han_sungjae/status/1412039183841980417))
	- (17) This will enable an environment similar to eth2's proposed long-term future; to quote Vitalik’s Rollup-centric Ethereum Roadmap: “a single high-security execution shard that everyone processes, plus a scalable data availability layer” 
	  
	  ![](https://pbs.twimg.com/media/E5iQrawVEAQotoi.png) ([View Tweet](https://twitter.com/han_sungjae/status/1412039188740939779))
	- (18) If the tooling for building a reliable execution layer off of multiple off-chain scaling solutions or legacy execution layers comes out solid and simple, this scalable data availability technology seems very very promising. ([View Tweet](https://twitter.com/han_sungjae/status/1412039190724825096))
	- (19) TL;DR: Avail and Celestia provide a new blockchain architecture that allows a modular design where application-specific sovereign chains can benefit from shared security. ([View Tweet](https://twitter.com/han_sungjae/status/1412039192037629954))