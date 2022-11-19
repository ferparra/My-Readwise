title:: MEV: What Is It? What P... (highlights)
author:: [[@obaidkav on Twitter]]
full-title:: "MEV: What Is It? What P..."
category:: #tweets
url:: https://twitter.com/obaidkav/status/1403801627207909387

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- MEV: What is it?
	  
	  What projects address it? 
	  
	  How do ETH2 and EIP-1559 affect it?
	  
	  I've been seeing LOTS of discussion across crypto chats about MEV. 
	  
	  It's an interesting topic with _huge ramifications_ for the #Ethereum ecosystem, so I've summarized EVERYTHING here.
	  
	  Thread 👇 ([View Tweet](https://twitter.com/obaidkav/status/1403800791220170755))
		- **Note**: Thread
	- MEV stands for Maximal [or Miner] Extractable Value.
	  
	  Generally, MEV is:
	  
	  The value that extracted by participants in a network who profit from their selfish preference of how events take place on-chain;
	  
	  Where they can economically express OR influence the order of events.
	  
	  1/X ([View Tweet](https://twitter.com/obaidkav/status/1403800795695435776))
	- Miners or validators are in a particularly alpha position to benefit from MEV;
	  
	  Because they're the ones who actually _produce_ blocks by ordering transactions, then _propose_ blocks to the network. 
	  
	  They can reorder, include, or censor transactions to their preference.
	  
	  2/X ([View Tweet](https://twitter.com/obaidkav/status/1403800800401502214))
	- MEV is extracted today mainly by making near-guaranteed arbitrages that ensure profits in a bundle of transactions. 
	  
	  It often involves DEX arbitrage; buying on one exchange, selling on another for higher...
	  
	  But making sure one gets those juicy prices through MEV influence.
	  
	  3/X ([View Tweet](https://twitter.com/obaidkav/status/1403800802997768192))
	- In the past, generalized frontrunning (i.e., inserting one tx before another) has caused user transactions to fail and waste gas.
	  
	  That forced dApps to use high slippage limits, so transactions could still execute if the order needed to deviate slightly from the quote price.
	  
	  4/X ([View Tweet](https://twitter.com/obaidkav/status/1403800805652807680))
	- Though high slippage limits allow for a more malicious form of MEV: sandwich attacks. 
	  
	  Sandwich attacks involve buying an asset _some user_ is trying to buy _before them_, then selling it to them right at their slippage limit. 
	  
	  Guaranteeing huge scalps at the user's cost.
	  
	  5/X ([View Tweet](https://twitter.com/obaidkav/status/1403800808228012033))
	- Another form of controversial MEV is in the collateralized lending space: 
	  
	  When a user is trying to repay a loan during a flash crash to prevent liquidation, then an extractor frontruns them with a liquidation.
	  
	  Price oracle updates and derivatives trades get frontrun too.
	  
	  6/X ([View Tweet](https://twitter.com/obaidkav/status/1403800810795016196))
	- The ever-growing complexity, interactivity, volumes, and liquidity across DeFi has given MEV extraordinary scale.
	  
	  The most sophisticated bot operators and the miners working with them are raking in between $1M-5M per day.
	  
	  🤯 Over $750M in MEV extracted to date on Ethereum.
	  
	  7/X ([View Tweet](https://twitter.com/obaidkav/status/1403800813483573252))
	- One company at the frontier of researching & developing in the MEV space is #Flashbots. 
	  
	  They've created is a model for detecting MEV transactions as they go through.
	  
	  Real-time MEV stats are transparently visible at: https://t.co/ZERJqJyxho
	  
	  8/X ([View Tweet](https://twitter.com/obaidkav/status/1403800820127252484))
	- A more important product they've shipped consists of MEV-Geth & a relay network.
	  
	  MEV-Geth is a modified Geth client.
	  
	  It includes a direct channel for MEV extractors to bid for tx inclusion with miners, _privately_.
	  
	  This prevents MEV bot gas wars from clogging Ethereum...
	  
	  9/X ([View Tweet](https://twitter.com/obaidkav/status/1403800822924951561))
	- Flashbots' solutions are a direct response to a dangerous direction that MEV was heading.
	  
	  MEV extractors were cutting backchannel deals with miners to have an edge in the game.
	  
	  That could've eroded transparency, permissionlessness, and trust in Ethereum's fairness.
	  
	  10/X ([View Tweet](https://twitter.com/obaidkav/status/1403800825760264196))
	- Flashbots has changed that. 
	  
	  They have created a network effect that has convinced MEV extractors that it is better to play in a fair, open marketplace.
	  
	  Over 85% of hashrate has joined Flashbots, reducing the strain of MEV gas wars on #ETH.
	  
	  See: https://t.co/zB7isjuYKq
	  
	  11/X ([View Tweet](https://twitter.com/obaidkav/status/1403800828390129669))
	- When two bots send the same arbitrage in to miners on Flashbots...
	  
	  They bid up the _tip being paid to the miner to include the tx_ significantly, at times 80%+ of profits.
	  
	  Some bot operators split opportunities to prevent unnecessarily high tips. https://t.co/1uGuj8sgHJ
	  
	  12/X ([View Tweet](https://twitter.com/obaidkav/status/1403800830852186114))
	- But Flashbots' solution has more uses beyond just helping _extractors_ and _miners_.
	  
	  It's also created a direct channel for dApps to send transactions directly to miners:
	  
	  Avoiding the public mempool so generalized bots cannot frontrun, backrun, or sandwich attack _users_.
	  
	  13/X ([View Tweet](https://twitter.com/obaidkav/status/1403800833645481986))
	- .@archer_swap (https://t.co/hMGfEeHq2V) is a DEX aggregator that submits transactions directly to Flashbots or ArcherDAO miners (5% ETH hashrate) through their Relayer contract.
	  
	  It allows users to set low slippage transactions without risk of wasting gas on a failed tx.
	  
	  14/X ([View Tweet](https://twitter.com/obaidkav/status/1403800836220850186))
	- Also, on ArcherSwap, if a user's DEX trade has a price impact:
	  
	  Extractors _arbitrage the liquidity pool_ (backrun) to balance prices across DEXes, then share profits between users and miners.
	  
	  Using direct-to-miner channels also allows for zero cost order cancellation.
	  
	  15/X ([View Tweet](https://twitter.com/obaidkav/status/1403800839110774784))
	- .@_alchemistcoin's mistX is another DEX aggregator that works similar to ArcherSwap, but only sends trades to Flashbots miners directly. 
	  
	  It also doesn't require the user to have any ETH to trade ERC20s, a feature that ArcherSwap intends to add soon.
	  
	  16/X ([View Tweet](https://twitter.com/obaidkav/status/1403800845511270401))
	- Both reduce MEV, but could still be exploited by miners, in which case #Flashbots will boot them from the system.
	  
	  MEV-SGX will prevent this, having validators perform PoW on encrypted headers constructed in an enclave to prevent corrupt activity.
	  
	  https://t.co/cygytCzg6M
	  
	  17/X ([View Tweet](https://twitter.com/obaidkav/status/1403800847667056640))
	- https://t.co/m2RsX57Ltv is a user-facing tool that submits ERC20 transfers directly to Flashbots miners. 
	  
	  This could one to rescue ERC20s from a compromised wallet without alerting the hacker.
	  
	  It requires pasting in a private key, so if you use it, build from source.
	  
	  18/X ([View Tweet](https://twitter.com/obaidkav/status/1403800850422718469))
	- .@bloXrouteLabs's BackRunMe (https://t.co/YXei5WwW8f) also allows for directly submitting txs to miners.
	  
	  Here, like ArcherSwap, if the user's trade has a price impact, searchers arbitrage the liquidity pool and then share 25% of profit with the user.
	  
	  19/X ([View Tweet](https://twitter.com/obaidkav/status/1403800853027426308))
	- .@Keeper_DAO's Hiding Book again allows for submitting transactions to a private mempool:
	  
	  This one of Keeper miners, where users are deliberately frontrun and/or backrun by self-coordinating extractors.
	  
	  Here, users are rewarded based on MEV extracted in $ROOK tokens.
	  
	  20/X ([View Tweet](https://twitter.com/obaidkav/status/1403800855644672009))
	- .@sparkpool_eth, the largest mining pool by $ETH hashrate, launched https://t.co/7Xcf6VpMRR in 2020 where transactions go directly to miners.
	  
	  Supposedly, transactions will not have MEV extracted from them, as the network is a "public good."
	  
	  It's unknown how adopted it is.
	  
	  21/X ([View Tweet](https://twitter.com/obaidkav/status/1403800858161262600))
	- .@gnosisPM's @MEVprotection, another DEX aggregator, matches simultaneous CowSwap users off-chain; where one may coincidentally be buying an asset and another selling that same asset.
	  
	  If it can't match them off-chain, its backfall solver network executes the trade on AMMs.
	  
	  22/X ([View Tweet](https://twitter.com/obaidkav/status/1403800860912672768))
	- As it stands, CowSwap's backfall protects users from sandwich attacks by using low slippage and pushing risk to solvers.
	  
	  But it doesn't prevent a trade from being frontrun/backrun, since txs go to the public mempool. They aim to change that soon.
	  
	  23/X ([View Tweet](https://twitter.com/obaidkav/status/1403800863697784835))
	- .@1inchNetwork, the DEX aggregator, also launched an OTC trading solution.
	  
	  It allows users to submit limit orders to off-chain market makers.
	  
	  Their off-chain market makers likely submit transactions directly to miners to prevent frontrunning.
	  
	  24/X ([View Tweet](https://twitter.com/obaidkav/status/1403800869443940355))
	- .@project_shutter is a project that seeks to address MEV still using the public mempool, by using distributed key generation to keep trades encrypted then decrypting them after they're included in a block.
	  
	  They have not launched on mainnet yet, but it is one to watch.
	  
	  25/X ([View Tweet](https://twitter.com/obaidkav/status/1403800951111159818))
	- Okay, so that's all of the projects I know of seeking to address MEV.
	  
	  Now, let's talk about MEV on ETH2, after the merge happens.
	  
	  Since the issuance of new ETH post-merge is going down significantly, MEV extraction could have a huge impact on yields for stakers.
	  
	  26/X ([View Tweet](https://twitter.com/obaidkav/status/1403801011752509441))
	- Estimates predict that democratized MEV extraction could increase yields [ignoring tx fees] by 75.3% across the current 160K validators. 🤯
	  
	  Versus the 5.6% boost seen by ETH1 miners now.
	  
	  In practice, variance in MEV per block & block luck will favor larger stakeholders.
	  
	  27/X 
	  
	  ![](https://pbs.twimg.com/media/E3tNo4-WYAUOYYX.png) 
	  
	  ![](https://pbs.twimg.com/media/E3tNo5WXwAY3Y8x.png) ([View Tweet](https://twitter.com/obaidkav/status/1403801082753650694))
	- Validator pools can help smooth out the rewards variance, but this will also disincentivize solo validation.
	  
	  It also remains to be seen if or how validator pools as well as exchanges, protocol treasuries, and funds will distribute the MEV they extract.
	  
	  28/X ([View Tweet](https://twitter.com/obaidkav/status/1403801116798824451))
	- Exchanges like Kraken, Binance, and Coinbase will control a significant amount of validator slots.
	  
	  How they extract MEV may depend on regulatory forces.
	  
	  They may be able to reorder blocks they produce synergistically with their products (i.e., expediting withdrawals).
	  
	  29/X ([View Tweet](https://twitter.com/obaidkav/status/1403801141729767429))
	- Also, since validators for each block in each 32-block epoch are known 6.4 minutes in advance...
	  
	  Extractors will be in a better position to compute optimal MEV extraction more easily:
	  
	  Thanks to predictable guarantees of which blocks they'll extract from.
	  
	  30/X ([View Tweet](https://twitter.com/obaidkav/status/1403801172998246404))
	- Large validator pools and exchanges may be lucky enough to produce multiple consecutive block proposal slots in an epoch across their validator sets.
	  
	  This will allow for more sophisticated multi-block MEV extraction.
	  
	  31/X ([View Tweet](https://twitter.com/obaidkav/status/1403801203587354628))
	- Also, as transaction flow ports over to L2s like rollups, some MEV will be transported onto those layers.
	  
	  New MEV will exist within any L2, across L2s, between L2 and L1.
	  
	  Validators may even reorder batch proofs submitted by L2s & shards later on, to deepen extraction.
	  
	  32/X ([View Tweet](https://twitter.com/obaidkav/status/1403801234868420616))
	- Finally, there are some minor implications for MEV when EIP-1559 goes through later this summer.
	  
	  The basefee will force private transactions to pay an actual gas fee rather than simply directing a miner tip via the multicall. 
	  
	  It won't affect users much.
	  
	  33/X ([View Tweet](https://twitter.com/obaidkav/status/1403801260931928067))
	- Alright. We've gone through pretty much everything I've found about MEV.
	  
	  Now let's talk about the ethical debate surrounding MEV.
	  
	  It's a contentious debate; with some suggesting MEV is outright theft, while others suggest it is fundamental to most consensus games.
	  
	  34/X ([View Tweet](https://twitter.com/obaidkav/status/1403801281819561984))
	- You could generally say that MEV comes as a result of two things: validators producing blocks by ordering transactions, and priority gas auctions.
	  
	  The former is inherent most consensus games, while the latter is necessary for differentiating between spam & real txs.
	  
	  35/X ([View Tweet](https://twitter.com/obaidkav/status/1403801303537623041))
	- Some differentiate between:
	  
	  Good MEV; which makes DEXes more efficient and tightens spreads, and...
	  
	  Bad MEV; like malicious loan fruntrunning, censoring L2 batch proofs, or MEV extracted by doing multi-block reorgs, if the profits are lucrative enough.
	  
	  36/X ([View Tweet](https://twitter.com/obaidkav/status/1403801331790385155))
	- A key reason why trying to _remove MEV_ isn't a practical option is...
	  
	  Attempts to do so have resulted in extractors and miners establishing off-protocol channels for facilitating it.
	  
	  Like when a Geth update to prevent backruns just made miners use custom mining software.
	  
	  37/X ([View Tweet](https://twitter.com/obaidkav/status/1403801360974454793))
	- Some have suggested implementing a fair ordering scheme onto Ethereum to prevent malicious MEV. This isn't a near-term solution at all, but also... 
	  
	  @phildaian argues that this will still leave MEV on the table, and we need to think deeper to address the issue.
	  
	  38/X ([View Tweet](https://twitter.com/obaidkav/status/1403801388912676864))
	- Daian also suggests that there are small wins that dApps can make to prevent malicious MEV.
	  
	  MEV is now something all ETH developers need to think about when designing and building their solutions, to minimize it as much as possible.
	  
	  But it will always be there.
	  
	  39/X ([View Tweet](https://twitter.com/obaidkav/status/1403801420973883397))
	- .@el33th4xor suggests that no protocol-level MEV exists on Avalanche. Transaction inclusion may differ on Avalanche...
	  
	  But @phildaian argues that networks like Avalanche have same economic properties and consensus game implications as Ethereum.
	  
	  40/X
	  
	  https://t.co/9BVmPfzD9G ([View Tweet](https://twitter.com/obaidkav/status/1403801483435515906))
	- In other words, while Avalanche may make good strides, there still exists a power structure allowing certain parties to behave to their preference.
	  
	  For instance, biasing which transactions to propagate first.
	  
	  They can still influence outcomes probabilistically.
	  
	  41/X ([View Tweet](https://twitter.com/obaidkav/status/1403801529988026374))
	- The Flashbots team argues that some form of MEV will exist on every blockchain and every L2. 
	  
	  Cross-chain AMMs like @AnyswapNetwork and @THORChain will leave MEV on the table to extract from networks like Avalanche too. 
	  
	  It just won't manifest until you have huge volume.
	  
	  42/X ([View Tweet](https://twitter.com/obaidkav/status/1403801556261220353))
	- Anyways, that's a wrap!
	  
	  That's everything I've been able to find on MEV across Telegram groups, Discord servers, articles, and direct messages with the experts.
	  
	  I hope this has helped offer some brevity on the topic!
	  
	  43/X ([View Tweet](https://twitter.com/obaidkav/status/1403801580768534530))
	- NONE of what's above are my original thoughts.
	  
	  All credits go to the following people for the resources they've put out:
	  
	  @phildaian, @ObadiaAlex, @_charlienoyes, @gakonst, @bertcmiller, the entire Flashbots team, and the other teams mentioned in this thread. Thank you everyone! ([View Tweet](https://twitter.com/obaidkav/status/1403801627207909387))