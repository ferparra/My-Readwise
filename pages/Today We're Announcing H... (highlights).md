title:: Today We're Announcing H... (highlights)
author:: [[@NoahCitron on Twitter]]
full-title:: "Today We're Announcing H..."
category:: #tweets
url:: https://twitter.com/NoahCitron/status/1589739389545914368

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Today we're announcing Helios, a fast, portable, and secure Ethereum light client written in Rust.
	  
	  Helios syncs in two seconds, uses no storage, and provides trustless access to Ethereum.
	  
	  Code: https://t.co/CnGa92lcfN
	  
	  Post: https://t.co/BXtuBStKVV
	  
	  1/8 ([View Tweet](https://twitter.com/NoahCitron/status/1589739389545914368))
		- **Note**: Thread
	- Most users currently access Ethereum using a centralized RPC provider. These are nodes run by companies in the cloud, providing convenient access to chain data.
	  
	  When a wallet fetches your account balance, odds are its routing this request through a centralized provider.
	  
	  2/8 ([View Tweet](https://twitter.com/NoahCitron/status/1589739392196702208))
	- While these providers are convenient, users have no way to know that they are being served correct data. You just have to trust that the provider is being honest.
	  
	  In the blog post, we even describe a mechanism in which malicious providers can steal funds from their users.
	  
	  3/8 ([View Tweet](https://twitter.com/NoahCitron/status/1589739395329839104))
	- Users have traditionally solved this problem by running their own nodes — a time and resource-intensive endeavor that, at the very least, requires a constantly-online machine, hundreds of gigabytes of storage, and around a day to sync from scratch.
	  
	  4/8 ([View Tweet](https://twitter.com/NoahCitron/status/1589739397942898688))
	- Our solution is Helios, a light client that syncs in less than two seconds, requires no storage, and provides trustless access to Ethereum.
	  
	  Helios uses Ethereum’s new light client protocol to provide efficient access to the chain with the same functionality as a full node.
	  
	  5/8 ([View Tweet](https://twitter.com/NoahCitron/status/1589739400576913409))
	- Helios works together with your centralized RPC provider to create a verifiably correct local RPC on your machine.
	  
	  A good mental model for Helios is that it converts a centralized RPC that you may not fully trust into one that is provably safe.
	  
	  6/8 ([View Tweet](https://twitter.com/NoahCitron/status/1589739403139653632))
	- Helios is very lightweight. Users will have no trouble running it on low-cost hardware and mobile devices.
	  
	  This makes Helios a prime target to integrate into other applications. Imagine if your wallet had a light client build directly into it. Helios can do this!
	  
	  7/8 ([View Tweet](https://twitter.com/NoahCitron/status/1589739405731713024))
	- Check out the GitHub, which includes installation instructions that can get you using Helios in five minutes.
	  
	  Feel free to check out the code. We'd love to see community contributions, and intend to keep working on Helios ourselves.
	  
	  We can't wait to see what you build.
	  
	  8/8 ([View Tweet](https://twitter.com/NoahCitron/status/1589739408202207232))