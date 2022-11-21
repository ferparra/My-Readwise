title:: Vbuterin (highlights)
author:: [[reddit]]
full-title:: "Vbuterin"
category:: #articles
url:: https://www.reddit.com/user/vbuterin/

- Highlights first synced by [[Readwise]] [[Nov 20th, 2022]]
	- There's two uses of ZK-SNARKs: you can use them for privacy, or you can use them for scalability. ([View Highlight](https://read.readwise.io/read/01gj9f7xnnvfnpygtqewb8wtvv))
		- **Tags**: #[[ethereum]] #[[crypto]]
	- There are ZK-rollups that use ZK tech for privacy as well (these are sometimes called "ZK ZK rollups"). [AZTEC](https://aztec.network/) is the most famous one in this category. These have slightly less scalability, because [privacy techniques](https://vitalik.ca/general/2022/06/15/using_snarks.html) require storing more complicated on-chain data such as nullifiers; you need around 64 bytes on-chain per transaction. ([View Highlight](https://read.readwise.io/read/01gj9f8ps1pyxh5zcybp97jad0))
	- The limits on making block time faster have to do with safety and decentralization (specifically, avoiding scenarios where nodes with much better network connections have a large economic advantage, which risks leading to ethereum mining or staking centralizing on eg. AWS). ([View Highlight](https://read.readwise.io/read/01gj9fadebz2hex93vm84z1eac))
	- Our version of proof of stake attempts to give blocks a very high level of confirmation after even one slot, and this requires thousands of signatures (currently ~9100) per slot to get included in the next slot. ([View Highlight](https://read.readwise.io/read/01gj9fayn33sa1zngraceq9k48))
	- [single-slot finality](https://notes.ethereum.org/@vbuterin/single_slot_finality), which will mean that a single slot would actually finalize a transaction instead of just strongly confirming it as it does today. ([View Highlight](https://read.readwise.io/read/01gj9fbbk2y3hff0dh634jkm59))
	- Many people have the mentality that "if a blockchain gets 51% attacked, everything breaks, and so we need to put all our force on preventing a 51% attack from ever happening even once". I really disagree with this style of thinking; in fact, blockchains maintain many of their guarantees even after a 51% attack, and it's really important to preserve these guarantees. ([View Highlight](https://read.readwise.io/read/01gj9fd5zg9sgc3xnwc55c6r0m))
	- No one will 51% attack Ethereum just to steal 100 Solana-WETH (or, for that matter, 51% attack Solana just to steal 100 Ethereum-WSOL). But if there's 10 million ETH or SOL in the bridge, then the motivation to make an attack becomes much higher, and large pools may well coordinate to make the attack happen. ([View Highlight](https://read.readwise.io/read/01gj9feapqaj7jdfvq9v9279wv))