title:: Since EIP-1559 Went Live... (highlights)
author:: [[@PhABCD on Twitter]]
full-title:: "Since EIP-1559 Went Live..."
category:: #tweets
url:: https://twitter.com/PhABCD/status/1423292129049198592

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Since EIP-1559 went live, some blocks are 5% full while others are at 100%. I think this is actually normal.
	  
	  While I haven't investigated the mempool, I suspect most people are using wallets that still use the old gas price logic
	  
	  Notice how big blocks are followed by small ones 
	  
	  ![](https://pbs.twimg.com/media/E8CLwwOVkAoSgyC.jpg) ([View Tweet](https://twitter.com/PhABCD/status/1423292129049198592))
		- **Note**: Thread
	- This makes sense because when blocks are bigger than 50%, basefee increases, while if below, they decrease.
	  
	  If most people are using wallets that don't incorporate the new gas price logic, then a baseFee increase will mean most of the txns in the mempool *can't* be included. ([View Tweet](https://twitter.com/PhABCD/status/1423292130936623104))