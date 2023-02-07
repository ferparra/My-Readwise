title:: Controversial ZK Opinion... (highlights)
author:: [[@_bfarmer on Twitter]]
full-title:: "Controversial ZK Opinion..."
category:: #tweets
url:: https://twitter.com/_bfarmer/status/1473519099691028482

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Controversial ZK opinion: optimizing for proof size below ~100kb - at the cost of prover time, recursion efficiency, and Ethereum compatibility - doesn’t make sense for blockchains. From this perspective, FRI-based schemes are more attractive than ECC-based SNARKs. 🧵 ([View Tweet](https://twitter.com/_bfarmer/status/1473519099691028482))
		- **Note**: Thread
	- Right now, pairing-based proofs offer lower verification costs on Ethereum, so they’re a good fit for L2s. But this is changing with EIP-4488. ([View Tweet](https://twitter.com/_bfarmer/status/1473519100718682112))
	- For ZK L1s, where every transaction is verified with a proof, there's an argument that smaller proofs => higher throughput, because smaller proofs mean we can fit more tx in a block. ([View Tweet](https://twitter.com/_bfarmer/status/1473519101666545675))
	- But this is a mistake for two reasons: 1) it ignores recursion - there’s no reason why every node should download and verify every proof, and 2) past a few hundred TPS, compute is the bottleneck for verifying ECC-based SNARKs, not bandwidth. ([View Tweet](https://twitter.com/_bfarmer/status/1473519102761254915))
	- With recursion, we aggregate proofs with powerful, centralized provers, or with many validators each aggregating a subset of proofs in a block.
	  
	  In either case, throughput is no longer limited by bandwidth, even if proofs are “big,” say 100kb. ([View Tweet](https://twitter.com/_bfarmer/status/1473519103793143808))
	- So, under a certain size threshold, what should we optimize for? Prover performance and recursion efficiency. FRI lets us do both. ([View Tweet](https://twitter.com/_bfarmer/status/1473519104887865346))
	- With FRI, we can use small fields and exploit a space-time tradeoff between proof size and proving time. For example, when proving complex statements (Ethereum tx!), we can use a low blowup factor (fast+big proof). ([View Tweet](https://twitter.com/_bfarmer/status/1473519105856745472))
	- After we’ve aggregated all of the tx proofs, we can do the opposite and generate a small recursive proof with a high blowup factor (slow+small proof) to bridge to Ethereum. We only have to do this once for the final proof, and the circuit size is tiny. ([View Tweet](https://twitter.com/_bfarmer/status/1473519107039539200))
	- Recursive FRI gives us the best of both worlds - fast proofs when we're limited by proving time, and fast verification in environments like Ethereum where gas cost dominates. ([View Tweet](https://twitter.com/_bfarmer/status/1473519108092268550))
	- That's why we built Plonky2 earlier this year (and will be open sourcing it in a few weeks). 
	  
	  It’s a recursive [[SNARK]] based on PLONK + FRI. It's far faster than anything else - recursive proofs take 170ms on a Macbook Pro - and it allows us to take advantage of FRI’s flexibility. ([View Tweet](https://twitter.com/_bfarmer/status/1473519109103104002))
	- It’s also natively compatible with Ethereum, unlike other recursion schemes like Halo. Size-optimized proofs are 45kb, and after EIP-4488, it should be the cheapest recursive [[SNARK]] to verify on [[Ethereum]]. 
	  
	  We think it's the best approach for ZKP's on blockchains. @0xPolygon 🚀 ([View Tweet](https://twitter.com/_bfarmer/status/1473519110143283201))