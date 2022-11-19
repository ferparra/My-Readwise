title:: The Celestia Design 🧵 Th... (highlights)
author:: [[@CelestiaOrg on Twitter]]
full-title:: "The Celestia Design 🧵 Th..."
category:: #tweets
url:: https://twitter.com/CelestiaOrg/status/1465291689493688323

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- The celestia design 🧵
	  The core idea of Celestia is to decouple transaction execution (and validity) from the consensus layer, so that the consensus is only responsible for a) ordering transactions and b) guaranteeing their data availability. ([View Tweet](https://twitter.com/CelestiaOrg/status/1465291689493688323))
		- **Note**: Thread
	- This is the bare minimum that the consensus layer of a blockchain needs to do to enable useful applications, such as a cryptocurrency. In the case of PoS protocols, a minimal consensus execution layer is necessary, although this may also be implemented as an optimistic rollup. ([View Tweet](https://twitter.com/CelestiaOrg/status/1465291767964573696))
	- In Celestia, a block that has consensus is considered valid only if the data behind that block is available. This is to prevent block producers from releasing block headers without releasing the data behind them. ([View Tweet](https://twitter.com/CelestiaOrg/status/1465291833043394567))
	- Celestia reduces the problem of block verification to data availability verification, which we know how to do efficiently with sub-linear cost using data availability proofs. The proofs require each client to sample a very small number of random chunks from each block… ([View Tweet](https://twitter.com/CelestiaOrg/status/1465291906464698369))
	- in the chain, and will only work if there are enough clients in the network that are collectively sampling the entire chain. This leads to an interesting consequence: the more clients you have in the network, the greater the block size (and thus throughput) you can have securely. ([View Tweet](https://twitter.com/CelestiaOrg/status/1465291983963013123))
	- Unlike existing scaling designs such as sharding, in Celestia the end-user validation capacity of the chain increases with non-consensus nodes. This is a unique property, as it means nodes that are not producing blocks can contribute to the throughput and security of the network. ([View Tweet](https://twitter.com/CelestiaOrg/status/1465292086526177286))
	- Read the full article here 👇
	  https://t.co/rucNrL9xwF ([View Tweet](https://twitter.com/CelestiaOrg/status/1465292329577684996))