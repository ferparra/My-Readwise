title:: Solana Claims to Be Able... (highlights)
author:: [[@brockjelmore on Twitter]]
full-title:: "Solana Claims to Be Able..."
category:: #tweets
url:: https://twitter.com/brockjelmore/status/1433189610797113357

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- solana claims to be able to handle more transactions thanks to their parallel execution
	  
	  how big of a speed up could the evm get if it did something similar?
	  
	  i built a parallel evm execution engine to find out
	  
	  /thread ([View Tweet](https://twitter.com/brockjelmore/status/1433189610797113357))
		- **Note**: Thread
	- first, some background. the evm is “Virtual Machine”, or software that simulates hardware, that standardizes and simplifies what is possible to do on the Ethereum blockchain ([View Tweet](https://twitter.com/brockjelmore/status/1433189613636657152))
	- it has what are called Op Codes, that are simple instructions like Add, Subtract, Multiply, Store, Store to Memory, etc. 
	  
	  smart contracts are just a series of these operations coded in a high level language like solidity ([View Tweet](https://twitter.com/brockjelmore/status/1433189616228704257))
	- when you send a transaction, it gets placed in a block and the txs in the block execute serially.
	  
	  this is because if a transaction before yours changes the storage of a contract you also interact with, the outcome of your tx may be dependent on that change (think frontrunning) ([View Tweet](https://twitter.com/brockjelmore/status/1433189617654763522))
	- so how do you possibly execute in parallel if the state may change out from under you? “Optimistic parallelization”, or assume the result is going to be correct and rerun it if it’s not ([View Tweet](https://twitter.com/brockjelmore/status/1433189619068284929))
	- sounds simple enough. but it can get way deeper and have even more optimizations than what i did, like stack & memory snapshots to resume at sload points, static analysis for highly used contracts like uniV2/v3, etc. that doesn’t even need the snapshots to resume computation ([View Tweet](https://twitter.com/brockjelmore/status/1433189620888518666))
	- now a little bit about my implementation. say we get a block of txs, ~120 or so. the implementation spins up 1 thread per tx, and uses a concurrent hashmap implementation for reading state. 
	  
	  each thread processes their tx, recording state updates and state reads ([View Tweet](https://twitter.com/brockjelmore/status/1433189622654320643))
	- this is a lock-free hashmap implementation so there is no contention for reads. so each transaction assumes the current state is correct for its execution, and returns the needed data ([View Tweet](https://twitter.com/brockjelmore/status/1433189623774289925))
	- after all txs are processed, we check for read/write contention. if we find contention, we apply the changes for txs that were first in the ordered block, and we simply rerun the contentious txs ([View Tweet](https://twitter.com/brockjelmore/status/1433189626341175306))
	- so what is the best case speedup? well in theory it is proportional to the number of txs in a block such that the longest it takes is the highest gas tx duration. ([View Tweet](https://twitter.com/brockjelmore/status/1433189628241121287))
	- that assumes that every transaction’s state dependency is mutually exclusive such that no tx would ever affect another
	  
	  in reality this effectively never happens. so how long does it take in the worst case? ([View Tweet](https://twitter.com/brockjelmore/status/1433189629595996164))
	- (identical txs for example) well in theory it shouldn’t take much longer than running it serially. you could have the program run serially after the first contention failure and you would see just a slight overhead waiting for the highest gas tx to finish ([View Tweet](https://twitter.com/brockjelmore/status/1433189632397778945))
	- or you could continue to be optimistic and assume once the first batch of contention has cleared you’re not going to hit a bunch more and rerun the remaining txs in parallel again ([View Tweet](https://twitter.com/brockjelmore/status/1433189634272632835))
	- so to get to some numbers: in a 120 tx block, 0 contention resulted in a *5x speedup* on a first pass implementation
	  
	  in a 120 tx block with 100% contention and pessimistic about further parallelism resulted in a 17% slowdown ([View Tweet](https://twitter.com/brockjelmore/status/1433189636940222465))
	- i’ll likely open source this in the future. if you want to help test against real world data or pick up the idea and firm it up into production quality lmk
	  
	  with a bit of optimization work i could see this consistently resulting in 3x block execution time for most blocks
	  
	  /end ([View Tweet](https://twitter.com/brockjelmore/status/1433189638496264197))