title:: Let's Have a Conversatio... (highlights)
author:: [[@euler_mab on Twitter]]
full-title:: "Let's Have a Conversatio..."
category:: #tweets
url:: https://twitter.com/euler_mab/status/1459314402059034634

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Let's have a conversation about how to manipulate @Uniswap v3's time-weighted average price (TWAP) oracles. 
	  
	  How would you do it? How much would it cost? How much profit could you make? 
	  
	  Read on, or check out my short paper here: 
	  
	  https://t.co/IXDzQgRHrM ([View Tweet](https://twitter.com/euler_mab/status/1459314402059034634))
		- **Note**: Thread
	- Let us suppose you are an attacker that plans to manipulate a Uni v3 TWAP oracle for DAI-USDC in order to trick a lending protocol into allowing you to withdraw more assets than you should be able to, given the initial USDC you have at your disposal. https://t.co/OCjIiVJjYM ([View Tweet](https://twitter.com/euler_mab/status/1459314418286800898))
	- Uniswap v3's TWAP oracles are calculated as the geometric mean of the spot price over the last n blocks. 
	  
	  To manipulate a geometric mean TWAP therfore requires you to manipulate the spot price on at least one block within the TWAP window. ([View Tweet](https://twitter.com/euler_mab/status/1459314419746230273))
	- The TWAP value is updated on the first transaction of block i using the last trade price on block i - 1. 
	  
	  This means you are required to expose any spot price manipulation efforts to arbitrageurs for at least one block. ([View Tweet](https://twitter.com/euler_mab/status/1459314420757188611))
	- Let us assume that the TWAP is calculated over n = 144 blocks (roughly a 30 minute window) and that the initial spot price is 1 USDC per DAI. ([View Tweet](https://twitter.com/euler_mab/status/1459314421629599749))
	- You can only really begin to gain a borrowing advantage of any kind on a lending protocol if you can manipulate the price higher (lower) than the maximum loan-to-value (LTV). ([View Tweet](https://twitter.com/euler_mab/status/1459314422720176129))
	- Suppose the DAI collateral factor is 0.75 (as it is on @compoundfinance ) so that you will need to push the TWAP to at least $1.35 ($1 / 0.75) to deposit DAI and borrow more than you should ordinarily be able to. ([View Tweet](https://twitter.com/euler_mab/status/1459314423638765572))
	- Most attackers would prefer to carry out their activities within a single atomic transaction, since this will usually enable them to ensure a risk-free return. 
	  
	  Here, however, you need to take on some market risk because your attack will span a minimum of two blocks. ([View Tweet](https://twitter.com/euler_mab/status/1459314424670474246))
	- Let us therefore first consider the minimal 'single-block' attack in which you want to limit your exposure by manipulating the spot price on a single block i, in order to use the manipulated TWAP on block i + 1. ([View Tweet](https://twitter.com/euler_mab/status/1459314425744273412))
	- There is a nice equation we can use in the paper above that describes the spot price manipulation that you need to achieve a given TWAP price. ([View Tweet](https://twitter.com/euler_mab/status/1459314426813812747))
	- We find that you need to manipulate the spot price to an eye-watering
	  
	  5,862,227,430,474,700,000 USDC per DAI
	  
	  in a single block, to achieve your aim. ([View Tweet](https://twitter.com/euler_mab/status/1459314427803615232))
	- The cost of this attack depends on how much slippage you face, and the amount of arbitrage you come up against. 
	  
	  We can provide estimates if we assume the attack takes place in a Uni v2 pool with $100k liquidity in it (equations for this in the paper). ([View Tweet](https://twitter.com/euler_mab/status/1459314428772499461))
	- We find that you need to swap a cool 
	  
	  121,060,185,709,756 USDC 
	  
	  into the pool, to achieve your aim. ([View Tweet](https://twitter.com/euler_mab/status/1459314429787582464))
	- This is currently more USDC than there is in the universe, so if you pull off this attack, we know that you are in fact @justinsuntron. ([View Tweet](https://twitter.com/euler_mab/status/1459314430798352386))
	- (all jokes aside, the up-front capital requirements here make pulling this attack off in an anonymous fashion much harder than a flash loan exploit) ([View Tweet](https://twitter.com/euler_mab/status/1459314431624687619))
	- Ok, so what about if you perform a 'multi-block' attack and spread your spot price manipulation over, say, 10 blocks? We now find that you need to manipulate the spot price to a mere
	  
	  75 USDC per DAI
	  
	  in each of 10 blocks, to achieve your aim. ([View Tweet](https://twitter.com/euler_mab/status/1459314432564248578))
	- The price manipulation is looking a lot more feasible for you, but what about the arbitrage cost? We now find that you need to swap in 
	  
	  383,884 USDC
	  
	  per manipulated block, and you will get back 44,238 DAI back from the swap. Over all ten blocks, your net cost is 3,396,454 USDC. ([View Tweet](https://twitter.com/euler_mab/status/1459314433570873349))
	- One could argue that this is a pretty cheap price to pay to manipulate a DAI-USDC price oracle, but wait. This is only a hypothetical example in which there is a measely $100k liquidity in the pool, and there is much else to consider. ([View Tweet](https://twitter.com/euler_mab/status/1459314434564841476))
	- First, how are you actually going to profit from this attack? The DAI oracle lags the current price, and everyone can see where it is moving to. You are not alone, anon, in your quest to get a return from this attack. ([View Tweet](https://twitter.com/euler_mab/status/1459314435533721608))
	- This is not like a flash loan attack where you can earn guaranteed profit from the attack or cancel the transaction. You need to do this over half an hour! ([View Tweet](https://twitter.com/euler_mab/status/1459314436594802689))
	- The lagging, slow moving nature of the TWAP might even mean that the profit opportunity from the attack becomes a kind of dutch auction, with people withdrawing the available plunder before you get chance to. https://t.co/TQR0yiw8SS ([View Tweet](https://twitter.com/euler_mab/status/1459314443578482695))
	- Which raises another point. If people can see you doing this ahead of time, you can be sure there will be at least some people: a) looking to profit from you by increasing the cost of your attack; and b) be people looking to defend against your attack. ([View Tweet](https://twitter.com/euler_mab/status/1459314444799037440))
	- Even if you miraculously get to the block you were hoping for intact, you still need to flash loan some DAI, deposit it, borrow some other assets, sell them, and repay the flash loan. You only got 1 shot, 1 opportunity... wait, did you set the gas fee right? https://t.co/Ft65azlFRc ([View Tweet](https://twitter.com/euler_mab/status/1459314451606343682))
	- Then there's the issue of real life liquidity getting in the way. We used a hypothetical value of $100k in our example because that's what @eulerfinance is exploring for a level of protocol-owned liquidity that might help guard against this kind of attack. 
	  
	  Stay tuned on this. ([View Tweet](https://twitter.com/euler_mab/status/1459314452990418951))
	- But to carry out this attack on @Uniswap today would have taken you 3,050,000,000 USDC to get to a 75 USDC per DAI price. You would have gotten just 40,746,500 DAI back. Then you would have had to repeat this for 10 blocks. ([View Tweet](https://twitter.com/euler_mab/status/1459314453951004672))
	- Perhaps you could try to use flashbots to buy up block space to limit arbitrage. But the arbitrage opportunity emerges on the next block. ([View Tweet](https://twitter.com/euler_mab/status/1459314454844391429))
	- Searchers will spot this and bid up the bundle cost to the value of the arbitrage opportunity. Better hope you have some miner friends to help you. ([View Tweet](https://twitter.com/euler_mab/status/1459314455762907140))
	- If you've pulled it off so far without losing millions of dollars or being exposed and facing jail time, that's impressive. How much could you stand to make if you alone were somehow able to profit from the attack? ([View Tweet](https://twitter.com/euler_mab/status/1459314457000267784))
	- Realistically, you might be able to use the manipulated TWAP to flash loan $1b DAI, get $1.35b worth of deposits, borrow up to $1.032b assets (after LTV), sell them, paying slippage and fees, and repay your loan to get, maybe, $15-20m income (before costs, as above). ([View Tweet](https://twitter.com/euler_mab/status/1459314458069766149))
	- All things considered, to pull off a this attack would be unlike anything we have seen yet in DeFi. Let me know if you fancy giving it a go. ([View Tweet](https://twitter.com/euler_mab/status/1459314459093180417))
	- With thanks to Doug Hoyte, @bantg, @Mudit__Gupta, @bertcmiller, and @NoahZinsmeister for reading earlier drafts of the article above and providing helpful feedback. 
	  
	  And thanks to @0xalpharush for forcing me to finally publish it! ([View Tweet](https://twitter.com/euler_mab/status/1459314460087267332))