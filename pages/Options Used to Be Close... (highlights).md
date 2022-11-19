title:: Options Used to Be Close... (highlights)
author:: [[@krugermacro on Twitter]]
full-title:: "Options Used to Be Close..."
category:: #tweets
url:: https://twitter.com/krugermacro/status/1347516442674163719

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- Options used to be close to irrelevant for bitcoin's price.
	  
	  Until now.
	  
	  At current price levels, hedging large option notionals has a major impact on price.
	  
	  Here's a quick thread on options 👇
	- Let's start with the meaning of delta.
	  
	  Delta is the rate of change of an option's price relative to a change in the price of its underlying.
	  
	  For example, the price of a 50 delta option will move 50% as much as the underlying.
		- **Tags**: #[[favorite]]
	- For practical purposes, think of it as how much of the underlying you have:
	- An option where the option's strike (i.e. exercise price) is equal to current spot price is known as an at-the-money option (ATM). ATM options have a delta of 50, while deep in the money options have a delta of close to 100.
	- Can also think of delta as probability. A 50 delta option has a 50% chance of expiring in the money.
	  
	  For a call, the higher price goes => the more in the money the call => the higher the delta. 
	  
	  Once delta gets close to 100, odds are ~100% the option will expire in the money.
	- Gamma is the rate of change of an option's delta relative to a change in the price of its underlying.
	  
	  When you buy an option, you are long gamma.
	  
	  That means the further in the money the option goes, the faster the option's price will increase.
	  
	  That's positive convexity.
	- Can also think of Delta as speed and Gamma as acceleration.
	- Delta and Gamma together with Vega and Theta are part of *the Greeks*.
	  
	  The greeks all measure the sensitivity of an option to various changes.
	  
	  There are other greeks, such as Rho, Volga and Vanna, but understanding these is not necessary now.
	- Vega is the rate of change of an option's price relative to a change in its implied volatility.
	  
	  Theta is the rate of change of an option's price relative to a change in time to expiry.
		- **Tags**: #[[favorite]]
	- When buying an option, a trader is long gamma (convexity), long vega (volatility), and short theta (time decay).
	  
	  The option loses value as time passes. A trader who is long an option compensates time decay with convexity.
		- **Tags**: #[[favorite]]
	- Imagine an options seller (a dealer) who wants to hedge his delta exposure. By doing so he becomes delta neutral. 
	  
	  Say he sold a BTC call, so he buys bitcoin to hedge. As price goes up, to remain delta neutral, he buys more bitcoin.
	- The dealer is short gamma. So the more price goes up, the more the dealer has to buy to remain delta neutral, generating on the extremes what is known as a Gamma Squeeze.
	  
	  Gamma is the key. 
	  
	  Or more precisely, the gamma position of those who hedge their delta (mostly dealers).
	- When dealers gamma profile is negative, they will buy on the way up, and sell on the way down, amplifying market moves. 
	  
	  Conversely, when dealers have positive gamma, they will buy on the way down, and sell on the way up, dampening moves.
	  
	  TL;DR Negative Gamma = Violent Moves
	- This shows why this is relevant now
	  
	  https://t.co/LJ6eYYRctX