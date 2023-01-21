title:: 1/N the Sui Blockchain... (highlights)
author:: [[@tracecrypto1 on Twitter]]
full-title:: "1/N the Sui Blockchain..."
category:: #tweets
url:: https://twitter.com/tracecrypto1/status/1546498905856253954

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- 1/n The Sui Blockchain
	  
	  What you need to know about the next major L1:
	  
	  🧵👇 
	  
	  ![](https://pbs.twimg.com/media/FXY_HcKWAAgUJ3n.png) ([View Tweet](https://twitter.com/tracecrypto1/status/1546498905856253954))
		- **Note**: Thread
	- 2/n In this thread I'll give an overview of Sui's:
	- 3/n Tech:
	  
	  Building and extending on years of research at Meta, Sui is different from any blockchain we've seen. ([View Tweet](https://twitter.com/tracecrypto1/status/1546498908494462976))
	- 4/n To start, the blockchain is extremely high-performance. 
	  
	  Early results running Sui on a MacBook pro were able to process over 120K token transfers per second. ([View Tweet](https://twitter.com/tracecrypto1/status/1546498909513650177))
	- 5/n Key to Sui's performance is transaction parallelization.
	  
	  In most blockchains, transactions must be ordered and placed into a block to be executed sequentially. 
	  
	  Sequential execution unnecessarily restricts throughput on these chains – most transactions are independent. ([View Tweet](https://twitter.com/tracecrypto1/status/1546498910759387142))
	- 6/n Because Sui requires that dependencies of transactions be explicitly stated, it’s able to process them in parallel. 
	  
	  In the minority of cases where transactions are intertwined, Sui still allows them to be ordered and executed sequentially. ([View Tweet](https://twitter.com/tracecrypto1/status/1546498912017698816))
	- 7/n This is done by using 2 different paths to consensus:
	- 8/n Since independent transactions can be validated in parallel, Sui can increase throughput linearly with more machines per validator. 
	  
	  Sui Scales. ([View Tweet](https://twitter.com/tracecrypto1/status/1546498914286800896))
	- 9/n Sui doesn’t just have high-throughput. 
	  
	  It has low-latency too. 
	  
	  Its consensus algorithms focus on minimizing the communication that’s needed between validators to process transactions. ([View Tweet](https://twitter.com/tracecrypto1/status/1546498915356262400))
	- 10/n This leads to simple transfers being validated nearly immediately, while complex transactions are executed within 2-3 seconds.
	  
	  Of course, we’ll need to see how the network performs in public deployment, but early results are extremely promising. ([View Tweet](https://twitter.com/tracecrypto1/status/1546498916560113665))
	- 11/n Sui uses the Move VM and the Move programming language for its smart contracts. 
	  
	  Move is memory-safe like Rust, but is more expressive than other smart contract languages.
	  
	  I wrote a quick intro to Move here 👇
	  
	  https://t.co/zcnrVw13vy ([View Tweet](https://twitter.com/tracecrypto1/status/1546498917684203520))
	- 12/n Sui uses a minor variation of Move to improve network performance and ease the developer experience
	  
	  You can learn more about how Sui’s Move differs from normal Move here 👇
	  
	  https://t.co/JTlTzrDZYi ([View Tweet](https://twitter.com/tracecrypto1/status/1546498919164698625))
	- 13/n While storage on most blockchains is centered around accounts, Sui’s storage is designed around objects. 
	  
	  Each object is owned by an address and is mutable by default, but can be made immutable or shared between multiple addresses. ([View Tweet](https://twitter.com/tracecrypto1/status/1546498920418877441))
	- 14/n Sui’s Move smart contracts can receive these objects as inputs, manipulate them, and return objects as outputs. 
	  
	  This is a fundamentally different smart contract programming paradigm than Solidity or Rust. ([View Tweet](https://twitter.com/tracecrypto1/status/1546498921521991681))
	- 15/n It’s way more intuitive – here’s how an engineer for Sui describes programming in Move:
	  
	  “When I’m at the bar explaining Move, I’d say, ‘So here is this bottle and here is this glass. Imagine both of them are NFTs and if we have a function, which would be like... ([View Tweet](https://twitter.com/tracecrypto1/status/1546498922692108289))
	- 16/n ‘pour water’ from this bottle to a glass, you literally pass these two together.’ The function does it and returns you the full glass.”
	  
	  Source: https://t.co/IQMUqUl5KC ([View Tweet](https://twitter.com/tracecrypto1/status/1546498923812032513))
	- 17/n This intuitive programming is perfect for dynamic NFTs and crypto games that constantly mix and modify digital objects ([View Tweet](https://twitter.com/tracecrypto1/status/1546498925095436288))
	- 18/n Tokenomics:
	  
	  The SUI token has a 10B total supply. It’s set to be distributed between the founding team, investors, a public sale, the Sui foundation, and future emissions. 
	  
	  The exact initial token distribution will be released in the coming weeks. ([View Tweet](https://twitter.com/tracecrypto1/status/1546498926127218689))
	- 19/n Sui’s token serves 4 roles:
	  
	  1. Staking / Security
	  2. Transaction fees
	  3. Governance
	  4. Unit of Account / Medium of Exchange ([View Tweet](https://twitter.com/tracecrypto1/status/1546498927305834497))
	- 20/n Most blockchains suffer from large fluctuations in gas costs due to changing network demand.
	  
	  To keep gas prices low and predictable, Sui implements a novel gas market design: ([View Tweet](https://twitter.com/tracecrypto1/status/1546498928354512898))
	- 21/n Sui runs in epochs. Every epoch (24 hours), the validator set changes. 
	  
	  At that time, the new epoch’s validators vote on a reference gas price for the entire epoch. ([View Tweet](https://twitter.com/tracecrypto1/status/1546498929486962688))
	- 22/n The protocol then provides a number of incentives to validators to keep transaction fees close to the reference price throughout the entire epoch. 
	  
	  By providing more stable gas prices, transactions submitted to Sui are processed at more predictable speeds. ([View Tweet](https://twitter.com/tracecrypto1/status/1546498930602565632))
	- 23/n This creates a better user experience.
	  
	  But how do gas prices stay low during network congestion? ([View Tweet](https://twitter.com/tracecrypto1/status/1546498931873415168))
	- 24/n Because the network’s throughput scales linearly with more workers, validators can add more workers proportionally to increases in network demand.
	  
	  This keeps prices close to the reference price. ([View Tweet](https://twitter.com/tracecrypto1/status/1546498932959846403))
	- 25/n Sui also addresses state bloat. 
	  
	  Whenever a user submits data on-chain, they must pay both gas fees and fees to Sui’s “storage fund”. 
	  
	  This fund covers the real-world cost for validators to store the user’s data. ([View Tweet](https://twitter.com/tracecrypto1/status/1546498934214135809))
	- 26/n As the network matures and the cost of storage increases, validators are paid out through the storage fund. 
	  
	  Additionally, once a user no longer needs to store that data, they can delete it and receive a rebate from the storage fund. ([View Tweet](https://twitter.com/tracecrypto1/status/1546500230149021697))
	- 27/n The full economics behind the storage fund are fascinating.
	  
	  You can hear more on @Mysten_Labs recent AMA:
	  
	  https://t.co/BRUzzReWcY ([View Tweet](https://twitter.com/tracecrypto1/status/1546500231298162691))
	- 28/n See an overview of Sui’s tokenomics here: 
	  
	  ![](https://pbs.twimg.com/media/FXZE-mLWAAE3fyD.jpg) ([View Tweet](https://twitter.com/tracecrypto1/status/1546500236155273216))
	- 29/n Team:
	  
	  Sui is built by @Mysten_Labs, a company building foundational infrastructure for Web3.
	  
	  The business was founded by @EvanWeb3 @EmanAbio, @b1ackd0g, @GDanezis, @kostascrypto – all of whom were formerly building Novi or Diem at Meta. ([View Tweet](https://twitter.com/tracecrypto1/status/1546500237820321793))
	- 30/n These scientists and engineers are the original minds behind many of the breakthroughs at Meta underlying Sui including the Move programming language and the Narwhal/Tusk mempool and BFT consensus that are now being implemented on other blockchains. ([View Tweet](https://twitter.com/tracecrypto1/status/1546500238986432512))
	- 31/n The team is targeting 4 key applications for Sui:
	  1. Gaming
	  2. DeFi
	  3. Commerce
	  4. Social ([View Tweet](https://twitter.com/tracecrypto1/status/1546500240160833540))
	- 32/n All 4 applications will heavily leverage Sui’s high-throughput and low-latency to deliver the best user experience. 
	  
	  But gaming and social applications are uniquely well positioned to build on Sui. ([View Tweet](https://twitter.com/tracecrypto1/status/1546500241196781576))
	- 33/n [[Gaming]] can leverage Move’s safety and expressivity around digital objects.
	  
	  And [[social media]] applications can leverage Sui's data storage economics to store all their data directly on-chain. ([View Tweet](https://twitter.com/tracecrypto1/status/1546500242354364416))
	- 34/n Sui is currently running a public devnet and is launching its incentivized testnet next month. 
	  
	  Expect more details on mainnet launch in the coming months. ([View Tweet](https://twitter.com/tracecrypto1/status/1546500243533008896))
	- 35/n If you’re interested in learning more, check out the Sui docs!
	  
	  https://t.co/Zml9WOrVTN ([View Tweet](https://twitter.com/tracecrypto1/status/1546500245428883458))
	- 36/n If you’re thinking of building on Sui or in the Move ecosystem, I’d love to hear from you! 
	  
	  My DMs are open. ([View Tweet](https://twitter.com/tracecrypto1/status/1546500247672741888))