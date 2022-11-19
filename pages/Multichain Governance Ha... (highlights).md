title:: Multichain Governance Ha... (highlights)
author:: [[@krzKaczor on Twitter]]
full-title:: "Multichain Governance Ha..."
category:: #tweets
url:: https://twitter.com/krzKaczor/status/1442563786192441353

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Multichain governance happens as we speak! 
	  
	  @MakerDAO holders just executed their first L2 spell on both @optimismPBC and @arbitrum!
	  
	  Short thread 🧵 
	  
	  ![](https://pbs.twimg.com/media/FAUAYnbVcAoFhpV.png) ([View Tweet](https://twitter.com/krzKaczor/status/1442563786192441353))
		- **Note**: Thread
	- 2/ Maker governance on L2 is represented by L2GovernanceRelay. This is a contract that will `delegatecall` desired L2 spell. It can be called only via a cross-chain message coming from L1GovernanceRelay. 
	  Finally, L1GovernanceRelay can be called only via an L1 spell. ([View Tweet](https://twitter.com/krzKaczor/status/1442563788792762375))
	- 3/ L2 Spells on both rollups were identical at this time and were meant to test the whole integration. 
	  
	  ![](https://pbs.twimg.com/media/FAUA7DhWYAM-j9j.jpg) ([View Tweet](https://twitter.com/krzKaczor/status/1442563796753596418))
	- 4/ L1 spell is quite straightforward too. The biggest challenge is setting up values related to the L2 gas (especially on Arbitrum it gets difficult)... but this is a topic for another time. 
	  
	  ![](https://pbs.twimg.com/media/FAUB0yMVIAA5q-d.jpg) ([View Tweet](https://twitter.com/krzKaczor/status/1442563803967725574))
	- 5/ To recap: contracts living on L2 can be fully managed by L1 governance via async messages. 
	  
	  No need for multisigs or any admin keys. Long live decentralization! 🔥🔥🔥
	  
	  If you're curious here are the execution traces: 
	  •https://t.co/Ck43xKKgu9
	  •https://t.co/MThACcs75Q ([View Tweet](https://twitter.com/krzKaczor/status/1442563806224261123))