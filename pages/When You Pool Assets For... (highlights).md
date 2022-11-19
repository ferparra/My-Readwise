title:: When You Pool Assets For... (highlights)
author:: [[@jonwu_ on Twitter]]
full-title:: "When You Pool Assets For..."
category:: #tweets
url:: https://twitter.com/jonwu_/status/1393307338245873666

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- When you pool assets for an Automated Market Maker (AMM), you actually *become* a market maker.
	  
	  What does that imply? Are you a sitting duck or a chad?
	  
	  👩‍🌾Yet Another Guide to Yield Farming
	  Part 2: Markets & Fees ([View Tweet](https://twitter.com/jonwu_/status/1393307259904700422))
		- **Tags**: #[[favorite]]
		- **Note**: Thread
	- Imagine you're a merchant walking into the Roman Forum at the height of its glory (🚨 classics nerd 🚨).
	  
	  Today everyone is trading garum—ancient fermented fish sauce.
	  
	  As a garum seller, how would you find a buyer? ![](https://pbs.twimg.com/media/E1X5tY0WEAgN7RY.png) ([View Tweet](https://twitter.com/jonwu_/status/1393307262266003462))
	- The absolute simplest way would be for you to stand there and yell:
	  
	  "SELLING GARUM FOR 10 DENARI A JAR!"
	  (Denari = Roman bucks).
	  
	  This is called open outcry trading.
	  
	  As recently as 10 years ago, trading pits at the CME functioned on this "open outcry" model: ![](https://pbs.twimg.com/media/E1X5mYCWEAAcZLJ.png) ([View Tweet](https://twitter.com/jonwu_/status/1393307268796583936))
	- These types of markets are hard to navigate.
	  
	  Back in Rome, all you can hear in the echoing limestone canyons of the Forum is the din of other assholes shouting out their prices.
	  
	  So you call aside a boy to help you navigate the market. ([View Tweet](https://twitter.com/jonwu_/status/1393307271275425796))
	- You say something like:
	  
	  "Hey, boy, why don't you find me someone who wants to buy my garum for at least $10 a jar?"
	  
	  The "at least" part means you just put in a limit order—$10 is the limit of how low you'd sell. You'd sell for more of course, but $10 is your best price. ([View Tweet](https://twitter.com/jonwu_/status/1393307273250885637))
	- This is basically over-the-counter (OTC) trading.
	  
	  The seller sends "WTS 1 GARUM @ $10" to an OTC desk. The desk then takes the order and scurries around to buyers whispering, "Psst, wanna buy garum for $10?" 
	  
	  Hopefully someone does, and then buyer and seller exchange. ([View Tweet](https://twitter.com/jonwu_/status/1393307277634019328))
	- Now, the boy isn't stupid. 
	  
	  He's an energetic young lad providing a service, for both  buyer and seller.
	  
	  He decides to mark up your $10 garum and shop it around for $10.50.
	  
	  The $0.50 spread is what the boy pockets if he does his job well, and he makes it on every trade. ([View Tweet](https://twitter.com/jonwu_/status/1393307280817459203))
	- Unfortunately, the boy doesn't know the real-time price.
	  
	  He runs around frantically collecting market prices, but by the time he comes back, the price has shifted again.
	  
	  You as a trader can't execute your order quickly because you don't know the clearing price. ([View Tweet](https://twitter.com/jonwu_/status/1393307283011014658))
		- **Tags**: #[[favorite]]
	- This is where central limit order books (CLOB) come in. It's what it sounds like: a place where limit orders are written.
	  
	  Those who submit limit orders are "price makers" in that they make the book, and those who are willing to transact at any price are takers ("I'll take it"). ([View Tweet](https://twitter.com/jonwu_/status/1393307285062045701))
	- Market (taker) orders are filled at the best price for a given depth.
	  
	  So say you want to buy 1,000 $ETH and you'll do it at any price. The order book engine matches you with counterpart(ies) willing to sell 1,000 and settles the order.
	  
	  You've probably seen this screen: ![](https://pbs.twimg.com/media/E1X7XW5XEAcJZ8p.jpg) ([View Tweet](https://twitter.com/jonwu_/status/1393307290380509198))
	- It's easier to visualize in slo-mo and imagine a CLOB like a Tetris game.
	  
	  New limit orders are like blocks falling onto the playing field, and market ("taker") orders erase blocks from the playing field. https://t.co/c3mjvNSxQR ([View Tweet](https://twitter.com/jonwu_/status/1393307300614574083))
	- The other way to visualize this is like a ravine or canyon surrounding the market-clearing price.
	  
	  The steeper the walls, the more market depth and liquidity around the spot price & the harder it is for market orders to "dig out" and move price. ![](https://pbs.twimg.com/media/E1X-Ul5X0AUSGjs.jpg) ([View Tweet](https://twitter.com/jonwu_/status/1393307304985047044))
	- More depth means less price slippage.
	  
	  The better an exchange is able to concentrate liquidity around spot, the less impact large trades will have on price.
	  
	  In a CLOB, this is natural--people drop limit orders right around the spot price. So why AMM? ([View Tweet](https://twitter.com/jonwu_/status/1393307307690373126))
	- Recall x * y = k, which spreads liquidity evenly across the curve of prices from 0 to infinity. Seems dumb?
	  
	  But there's an advantage: liquidity bootstrapping.
	  
	  You can create a market for your token w/o relying on market makers or the permissions of CZ/SBF/BA to list your token. ([View Tweet](https://twitter.com/jonwu_/status/1393307309540089862))
		- **Tags**: #[[favorite]]
	- Disadvantages?
	  
	  Because liquidity is spread thinly rather than concentrated around the market clearing price, you have high price slippage and liquidity is inefficiently allocated.
	  
	  This is what liquidity-concentration projects like @UniswapV3 and @IntegralHQ are trying to solve. ([View Tweet](https://twitter.com/jonwu_/status/1393307312241184769))
	- As a pool provider, you're expressing a trade at the market price you can't change, and once you establish your position, arbs start trading against you.
	  
	  This was the cause for some debate back in the stone ages of 2020.
	  
	  Are you a sitting duck?
	  
	  https://t.co/LUhIlSpLuW ([View Tweet](https://twitter.com/jonwu_/status/1393307314015326212))
	- The savior is the 30 bps fee the AMM charges, and you hope value leakage from being traded against (impermanent loss) is offset by fee revenue.
	  
	  Volatility drives fee revenue but also IL. Confusing? See genius-level analysis from @Fiskantes explaining:
	  
	  https://t.co/tvUPh5ip6S ([View Tweet](https://twitter.com/jonwu_/status/1393307316171247626))
	- To add confusion, fee APR is commonly given as a one-year extrapolation of last 24h fees divided by the size of the pool.
	  
	  Not only are 24h fees an obviously poor guess at go-forward fee revenue, volume is heavily concentrated on days like the epic Vitalik-Elon tag-team rug. ([View Tweet](https://twitter.com/jonwu_/status/1393307318377459722))
	- So what to take away from all this?
	  
	  1) Fees are there to compensate you for IL risk, the same way if you were a traditional market maker you make a spread as compensation for price risk while trading the spread:
	  
	  https://t.co/cflrmKO5H2 ([View Tweet](https://twitter.com/jonwu_/status/1393307320034152460))
	- 2. It's a guess as to what the volume-TVL ratio of an exchange will be going forward.
	  
	  You're not only making a bet on the two asset prices but also the health and growth of *the exchange itself.*
	  
	  Pick a winner and your APR is steady or improving—pick a loser and you're 🦆ed. ([View Tweet](https://twitter.com/jonwu_/status/1393307321795809285))
	- 3) Take into consideration:
	- 4) Get smart and use tools:
	- Please raech out if you're building tools to help make entry/exit decisions, e.g.
	  
	  HODL value
	  + IL
	  + fees
	  + rewards
	  --> IRR on (USD / $ETH / $BTC) basis since hold
	  
	  And ofc feedback / ideas always welcome!
	  
	  ✌️ ([View Tweet](https://twitter.com/jonwu_/status/1393307334475198468))
	- BONUS SECTION:
	  
	  Non-trivial questions: