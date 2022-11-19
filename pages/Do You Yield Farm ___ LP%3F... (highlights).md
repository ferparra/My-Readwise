title:: Do You Yield Farm / LP?... (highlights)
author:: [[@jonwu_ on Twitter]]
full-title:: "Do You Yield Farm / LP?..."
category:: #tweets
url:: https://twitter.com/jonwu_/status/1389782687725010946

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- Do you yield farm / LP?
	  
	  It's sold as a passive strategy, but farming is the most nuanced, unintuitive, and poorly understood activity in Defi.
	  
	  It's more like putting on a short-term trade than buying fixed-income.
	  
	  🧑‍🌾 Yet Another Guide to Yield Farming
	  Part 1: Impermanent Loss ([View Tweet](https://twitter.com/jonwu_/status/1389782646000078850))
		- **Note**: Thread
	- Yield farming returns are dependent on the performance of the underlying assets, plus:
	  
	  1) Impermanent loss
	  2) Fee revenue
	  3) Rewards
	  
	  All of which are volatile, complex, and misleadingly advertised. ([View Tweet](https://twitter.com/jonwu_/status/1389782648118251522))
	- Part 1: Impermanent loss
	  
	  When you LP, not only are you taking a bet on each asset's price, you are also taking a bet on their *relative* pricing.
	  
	  Divergence from the starting ratio will incur what is called "impermanent loss" (universally considered a dumbass label). ([View Tweet](https://twitter.com/jonwu_/status/1389782650546708481))
	- To understand why, let's study the (soon-to-be-obsolete?) constant function market maker (CFMM) popularized by Uniswap.
	  
	  You know this as 
	  x * y = k
	  
	  Where x & y are the *quantities* of the two assets in the pool. ([View Tweet](https://twitter.com/jonwu_/status/1389782654564847616))
		- **Tags**: #[[defi]]
	- Because the value of both assets has to be the same in a 50/50 pool, the price is simply the ratio of x to y.
	  
	  Simple example:
	  
	  There are 50 $ETH and 100,000 $USDC in a pool. Price is a function of the $USDC: $ETH ratio, so in this case:
	  
	  1 $ETH = 2,000 $USDC (lol) ([View Tweet](https://twitter.com/jonwu_/status/1389782661779099649))
	- The two assets' values are equivalent because arbitrageurs make it so. Say the price of $ETH on Binance is 1,900 $USDC.
	  
	  An arbitrageur can buy $ETH for 1,900 $USDC on Binance, take it to Uniswap, and swap it for 2,000 $USDC. ([View Tweet](https://twitter.com/jonwu_/status/1389782664606109696))
		- **Tags**: #[[defi]]
	- Now the pool has 51 $ETH and 98,000 $USDC and its implicit price is 1 $ETH = 1,921.57 $USDC, which you'll note is closer to its off-Uniswap price.
	  
	  This is why the two sides of the pool trend toward equal value: arbitrageurs balance the pool. ([View Tweet](https://twitter.com/jonwu_/status/1389782666858409986))
		- **Tags**: #[[defi]]
	- If we know the two sides have equal value:
	  
	  P(x) * x = P(y) * y
	  
	  and we know the constant quantity function:
	  
	  x * y = k
	  
	  Then we can do some mf algebra: https://t.co/1ZQHmIkIf9 ([View Tweet](https://twitter.com/jonwu_/status/1389782670448676864))
	- This makes it visually obvious what the risk is: as the expression P(x) / P(y) trends to 0, so does the value of the pool.
	  
	  In fact, *any* change in that expression causes value leakage relative to HODLing.
	  
	  And where does this leakage go? Arbitrage. ([View Tweet](https://twitter.com/jonwu_/status/1389782672197754880))
		- **Tags**: #[[favorite]]
	- As the value of the two assets diverges, the pool continually rebalances toward the less valuable token.
	  
	  Arbitrageurs rebalance the pool and get paid with impermanent loss.
	  
	  Except IL is just as permanent as any other price move. A much better name would be "rebalancing loss." ([View Tweet](https://twitter.com/jonwu_/status/1389782674378788864))
	- Think about it like this: when you pool, you are expressing an opinion on price.
	  
	  If the price moves, arbitrageurs get the opportunity to trade against you.
	  
	  They have to pay you fees for the right to take you for a ride, but you're still getting taken for a ride. ([View Tweet](https://twitter.com/jonwu_/status/1389782675796463616))
	- Let's build up to some heuristics using these building blocks.
	  
	  1. Pool correlated assets to reduce IL risk. Volatile-stable are guaranteed to have IL.
	  
	  2.  Be comfortable owning either asset, because you are guaranteed to end up with more of the worse-performing one. ([View Tweet](https://twitter.com/jonwu_/status/1389782677285482498))
	- 3. Pool timing matters. Enter when the asset you ultimately want more of is trading at a near-term top relative to the other asset in the pair.
	  
	  As the more expensive (and more desirable) asset trades down, the pool rebalances toward it. ([View Tweet](https://twitter.com/jonwu_/status/1389782678669508611))
	- 4. IL is non-linear. Stare at the IL curve and ask yourself if you're being compensated sufficiently for pricing risk.
	  
	  E.g. if an asset appreciates 400% ("5x's") relative to its pool counterpart, IL is ~25%. If it appreciates 900% ("10x's"), IL is ~45%. https://t.co/oNn9ANpaq0 ([View Tweet](https://twitter.com/jonwu_/status/1389782683312697346))
	- 5. LPing is not a trade of indefinite length because you're compounding price risk. If *either* asset goes to 0 it zeroes out the value of the pool, and the longer you provide liquidity the more likely one of them goes to 0. ([View Tweet](https://twitter.com/jonwu_/status/1389782685732818944))
	- IL is just one of the reasons I think the marketing of pool APR as passive yield is behaviorally misleading.
	  
	  In Parts 2 & 3 we'll get into fees and rewards and how to think about APR degradation, how to time rewards, and how fees offset IL.
	  
	  ✌️ ([View Tweet](https://twitter.com/jonwu_/status/1389782687725010946))