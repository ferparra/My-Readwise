title:: Two Years Ago I Publishe... (highlights)
author:: [[@smpalladino on Twitter]]
full-title:: "Two Years Ago I Publishe..."
category:: #tweets
url:: https://twitter.com/smpalladino/status/1421901085279756300

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Two years ago I published my book "Ethereum for Web Developers", a book on building apps on Ethereum targeted at web2 developers.
	  
	  Yet a lot has changed in these past two years, so let's see how the book would look like if written today 🧵
	  
	  https://t.co/Y4oSeVw8A9 
	  
	  ![](https://pbs.twimg.com/media/E7uL5sLXIAQPEgX.jpg) ([View Tweet](https://twitter.com/smpalladino/status/1421901085279756300))
		- **Note**: Thread
	- 1⃣ Chapter 1 is an introduction to crypto, blockchains, and Ethereum.
	  
	  All fundamental concepts still apply, though back then there was a lot of attention around private blockchains which has subsided a lot.
	  
	  And I missed to mention collectibles among the main use cases! 🎨 ([View Tweet](https://twitter.com/smpalladino/status/1421901089306185735))
	- 2⃣ Chapter 2 goes hands-on building a complete dapp for a simple Counter contract.
	  
	  This chapter sets the toolchain to be used throughout the book:
	- Today I'd pick a different stack 🏗️
	  
	  While React still dominates in web2 and Metamask is the most widespread wallet, @ethersproject has replaced web3.js for me.
	  
	  And @HardhatHQ is stable (and awesome!) enough for contracts. It gets mentioned in the book, though as "buidler". 👷 ([View Tweet](https://twitter.com/smpalladino/status/1421901094687498240))
	- Aside from that, this chapter still holds strong! 💪
	  
	  For better or worse, the fundamentals of writing a dapp have changed little over these past two years. I'm surprised at how little the screenshots from Metamask have changed! 
	  
	  ![](https://pbs.twimg.com/media/E7uNdf-XIAIEjxG.png) ([View Tweet](https://twitter.com/smpalladino/status/1421901101079617540))
	- 3⃣ Chapter 3 unloads all the theory behind transactions and smart contracts.
	  
	  Transaction lifecycle hasn't changed, though a section on 1559-like transactions would come in handy today when discussing gas consumption! 
	  
	  ![](https://pbs.twimg.com/media/E7uNpuFWUAAchxh.jpg) ([View Tweet](https://twitter.com/smpalladino/status/1421901106712567809))
	- As for contracts, the book was written on solidity 0.5, and we're on 0.8 now. Revert reasons and safe arithmetic (bye SafeMath!) would be a good addition to this chapter.
	  
	  As for notable ERCs, I'd add ERC1155 next to ERC20 and ERC721.
	  
	  https://t.co/fdy4MYu6ZN ([View Tweet](https://twitter.com/smpalladino/status/1421901109287870466))
	- This chapter makes heavy use of @EthereumRemix as an environment for experimenting with smart contracts. 
	  
	  Remix is a great tool for onboarding new devs and for quick experiments. I'm happy to see it well maintained and that it keeps getting love from the ecosystem! ([View Tweet](https://twitter.com/smpalladino/status/1421901111452225537))
	- 4⃣ Chapter 4 discusses nodes, providers, querying, and events.
	  
	  This one can be brought verbatim to 2021. Without using additional services (I'll get to thegraph later!), the polling, filters, and subs options for events are the same. And calls don't have much magic to them! ([View Tweet](https://twitter.com/smpalladino/status/1421901113440223234))
	- This chapter includes a dapp to monitor ERC20 txs, using REP (v1, still active!) as an example.
	  
	  Fun fact: I once received a candidate application that included this very app claiming to be part of their portfolio. It did have nicer CSS though. 
	  
	  ![](https://pbs.twimg.com/media/E7uPAuyWEAE9bLA.png) ([View Tweet](https://twitter.com/smpalladino/status/1421901118343426052))
	- 5⃣ Chapter 5 goes to sending transactions, and discusses development nodes, wallets, and seed phrases.
	  
	  It includes gas estimation, tracking a transaction through its lifecycle, and handling generic errors; almost everything that you still need to account for today! 🗒️ ([View Tweet](https://twitter.com/smpalladino/status/1421901120516108298))
	- This chapter does not include capturing application-specific revert reasons, for a simple reason: they didn't exist back then!
	  
	  Today we have widespread revert strings, and custom errors were recently added to the language.
	  
	  https://t.co/uZ4NqSyY7r ([View Tweet](https://twitter.com/smpalladino/status/1421901122982318082))
	- 6⃣ Chapter 6 starts with more advanced topics: indexing and storage.
	  
	  The topic for this chapter was making use of external services for more optimized queries to the network and for storing large blobs of data. ([View Tweet](https://twitter.com/smpalladino/status/1421901125461155848))
	- The storage section makes heavy use of @IPFS, which is still the go-to storage solution 💽
	  
	  Pinning services are undervalued though, and many NFT holders have lost their metadata due to poor IPFS data management practices.
	  
	  https://t.co/evFnWXpWSj ([View Tweet](https://twitter.com/smpalladino/status/1421901127675695104))
	- As for indexing, it was a good excuse to talk about the challenges that arise from reorgs when tracking events, which is a topic I was particularly interested in.
	  
	  https://t.co/MyMc5QkY1p ([View Tweet](https://twitter.com/smpalladino/status/1421901129860931591))
	- However, for all practical purposes, the indexing section today could be replaced with a tutorial on using @graphprotocol, which today powers many of the main dapps in the space via its decentralized indexing network.
	  
	  https://t.co/i6RkZD0Zkj ([View Tweet](https://twitter.com/smpalladino/status/1421901132163686404))
	- This chapter also packs two pages with a discussion on decentralization which I still think is critical for the space.
	  
	  The TLDR is that decentralized protocols with centralized apps are a perfectly valid setup. We don't need to decentralize everything for the sake of it! 
	  
	  ![](https://pbs.twimg.com/media/E7uRB9VXoAQPknq.jpg) ([View Tweet](https://twitter.com/smpalladino/status/1421901138199253005))
	- For example, the Uniswap app is hosted and managed by a team, which allows to rapidly iterate on it.
	  
	  And if you don't like that a set of tokens were censored, you can use a different app that interacts with the same underlying decentralized protocol!
	  
	  https://t.co/gxU0JgQF0E ([View Tweet](https://twitter.com/smpalladino/status/1421901142762610699))
	- 7⃣ Chapter 7 packs several advanced topics around user onboarding.
	  
	  It covers keystores, mnemonics, single-use addresses, deterministic deployments, smart accounts, upgradeability, off-chain signatures, gasless meta-transactions, and wraps up with ENS. ([View Tweet](https://twitter.com/smpalladino/status/1421901145874866184))
	- If I had to change something on this chapter, it'd probably be breaking it down into more than one, since it packs a lot of info!
	  
	  Now, while onboarding has received less attention lately (I blame the bull market!), all concepts covered are still useful.
	  
	  https://t.co/Igp9STmcmV ([View Tweet](https://twitter.com/smpalladino/status/1421901150811459588))
	- 🧠 Smart accounts have been popularized through @argentHQ, @Dharma_HQ, @authereum, and others
	  
	  🆙 Upgradeability has become widely spread along with proper governance
	  
	  ⛽️ Meta-transactions are in use with both centralized relayers and through @opengsn
	  
	  https://t.co/zuDGAo5Gpq ([View Tweet](https://twitter.com/smpalladino/status/1421901153638440967))
	- As for @ensdomains, it is more popular than ever, now aiming at becoming a full sign-in-with-Ethereum solution ⚡️
	  
	  https://t.co/qGsiyj4CvV ([View Tweet](https://twitter.com/smpalladino/status/1421901156436033544))
	- The onboarding chapter also includes a little trick I love: you can let users interact with contracts without requiring a web3 wallet by setting up forwarding proxies, where each proxy calls a different function on the same set of main contracts! ([View Tweet](https://twitter.com/smpalladino/status/1421901158411550725))