title:: After a Successful Merge... (highlights)
author:: [[@kristofgazso on Twitter]]
full-title:: "After a Successful Merge..."
category:: #tweets
url:: https://twitter.com/kristofgazso/status/1576716946250543104

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- After a successful Merge, Account Abstraction (AA) is shaping itself to be the new 'big thing' on the horizon for Ethereum.
	  
	  The name makes it sound like a scary concept, but it is in fact very simple
	  
	  A thread 🧵 on what Account Abstraction is and why you should care about it: https://t.co/ogMkymC046 ([View Tweet](https://twitter.com/kristofgazso/status/1576716946250543104))
		- **Note**: Thread
	- Ethereum currently has two types of accounts:
	  
	  1. Externally Owned Accounts (EOAs): these accounts are simply controlled by a private key that derives to a specific address. They are what most users use to interact with the blockchain. Think @MetaMask, @rainbowdotme, and @Ledger ([View Tweet](https://twitter.com/kristofgazso/status/1576716950973349888))
	- 2. Smart Contract (SC) Accounts: these accounts are not controlled by any private key, rather they are controlled by their code. All the Defi protocols you know are of course controlled by SC Accounts, but also many wallets, like @argentHQ, and @safe. ([View Tweet](https://twitter.com/kristofgazso/status/1576716954198757378))
	- The issue with Ethereum is that EOAs get special privileges that SC accounts do not, despite the fact that EOAs are simply a specific type of account. The most notable example is the ability to initiate transactions. Only EOAs can do that.
	  
	  Why is this a problem? ([View Tweet](https://twitter.com/kristofgazso/status/1576716957432262656))
	- EOAs have a lot of their functionality hardcoded in the core Ethereum protocol. For instance:
	  
	  Signature verification: EOAs use a special signature scheme called ECDSA ([View Tweet](https://twitter.com/kristofgazso/status/1576716960796004353))
	- Replay protection: EOAs use a simple incrementing attribute called 'nonce' to disallow the same transaction from being included more than once
	  
	  Gas fees: EOAs must pay their gas purely with ETH and must do so only do so from their own balance at the start of the transaction ([View Tweet](https://twitter.com/kristofgazso/status/1576716964525113344))
	- But what if instead of hardcoding all these important functionalities of Ethereum accounts, you let people create accounts with their own methods for signature verification, replay protection, and gas payments with custom smart contract logic? ([View Tweet](https://twitter.com/kristofgazso/status/1576716967909941249))
	- This is what Account Abstraction represents: the move to generalize the notion of accounts on Ethereum. ([View Tweet](https://twitter.com/kristofgazso/status/1576716971264987136))
	- Imagine being able to pay fees in whichever token you desired, or having other users or contracts sponsor transactions for you. ([View Tweet](https://twitter.com/kristofgazso/status/1576716974486585344))
	- Or imagine deciding that your wallet should ditch ECDSA and verify the validity of transactions via a quantum-safe signature scheme, or a more distributed mechanism like multisig or social recovery. ([View Tweet](https://twitter.com/kristofgazso/status/1576716978470805504))
	- But Kristof, don't there already exist a lot of multisig and social recovery wallets live on Ethereum today?
	  
	  Yes, they exist. But they are forced to wrestle against the inefficiencies of the EOA system Ethereum uses. ([View Tweet](https://twitter.com/kristofgazso/status/1576716982216318976))
	- They must get an outside EOA to call the wallet's smart contract, getting the sender of the transaction to pay for all the gas fees this involves. ([View Tweet](https://twitter.com/kristofgazso/status/1576716985618305025))
	- But the sending EOA not only has to pay for the transaction payload, but also for the EVM execution of the gas, signature, and replay verification the SC wallet encodes.
	  
	  All the while EOAs get all these checks done by the protocol for free. It's just not a fair playing field. ([View Tweet](https://twitter.com/kristofgazso/status/1576716989975756801))
	- So how do we solve this? As @VitalikButerin mentioned, the best contender currently is EIP-4337, although I might be a bit biased 😅. ([View Tweet](https://twitter.com/kristofgazso/status/1576716993893666817))