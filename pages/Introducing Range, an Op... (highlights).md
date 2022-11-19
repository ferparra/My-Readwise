title:: Introducing Range, an Op... (highlights)
author:: [[@ohmzeus on Twitter]]
full-title:: "Introducing Range, an Op..."
category:: #tweets
url:: https://twitter.com/ohmzeus/status/1452765658232590342

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Introducing Range, an optimistic stablecoin swap protocol.
	  
	  (Note: Range is unaudited. Use at your own risk with money you can afford to lose.)
	  
	  Let's run through what it does 👇🧵 ([View Tweet](https://twitter.com/ohmzeus/status/1452765658232590342))
		- **Note**: Thread
	- Range is a stablecoin swap protocol that creates Range Pools.
	  
	  Range Pools make the optimistic assumption that tokens in the pool are always worth the same amount, and therefore always allows trades at a perfect 1:1 ([View Tweet](https://twitter.com/ohmzeus/status/1452765660430405637))
	- The fundamental idea, to abandon a pricing curve altogether, sounds kind of stupid when you first hear it. At least that's what I thought coming up with it. But the more you think about it, the more it makes sense. ([View Tweet](https://twitter.com/ohmzeus/status/1452765663169335305))
	- Instead of creating a pricing curve, tokens simply must remain within a pre-defined range.
	  
	  For example, the range for DAI in this first pool is 20%-70%. DAI must remain at least 20% of the pool, and no more than 70%.
	  
	  Any trade that would take it out of this range is rejected. ([View Tweet](https://twitter.com/ohmzeus/status/1452765665346179075))
	- Each token has one of these ranges. As long as whatever token you want to swap in/add, or swap out/remove stays within the range, you can do it. ([View Tweet](https://twitter.com/ohmzeus/status/1452765667309010944))
	- Why is this helpful?
	- What's the downside?
	- What's the usecase?
	  
	  My expectation is that (at least early on) the pool swings  from range extreme to range extreme as the pooled tokens fluctuate around peg. This should produce heavy fee volume from arbitrage ([View Tweet](https://twitter.com/ohmzeus/status/1452765673944494080))
	- Consider the following:
	  
	  The $10m TVL Range Pool can do a $3m trade from DAI to LUSD. The price between DAI and LUSD rises from 1.00 to 1.01. An arbitrageur can buy $3m LUSD from the RP and sell it for $3.03m on curve. In the process, the RP made a fee on 30% of its TVL. ([View Tweet](https://twitter.com/ohmzeus/status/1452765676058386439))
	- This started as a treasury allocation strategy for @OlympusDAO, and I see them as the largest beneficiary.
	  
	  Olympus has no concept of impermanent loss between stablecoins. It already treats 1 DAI as equal to 1 LUSD, and so it can never lose when allowing 1:1 swaps between them. ([View Tweet](https://twitter.com/ohmzeus/status/1452765678264627201))
	- RangePool will allow Olympus to productively deploy its reserves in an isolated environment where its exposure to different assets is defined and controlled. ([View Tweet](https://twitter.com/ohmzeus/status/1452765680546295815))
	- This is unlike existing stablecoin yield opportunities where you have some undefined level of exposure to various stablecoins, and generally take on 100% of their downside (if any token in a curve or v3 pool loses peg, LPs end up with only that token). ([View Tweet](https://twitter.com/ohmzeus/status/1452765682353967105))
	- I have deployed the first Range Pool on Ethereum. Ranges are as follows:
	- note: 0%-15% ranges allow volume from tokens with low LP exposure.
	  
	  We will use this pool as a testing ground. I hope we can prove this model, then propose it as a treasury strategy for Olympus. ([View Tweet](https://twitter.com/ohmzeus/status/1452765686539882498))
	- If you want to learn more or contribute, I made a discord: https://t.co/gYzZ1OV1L7
	  
	  Here are some docs: https://t.co/TgE8ayMp3L
	  
	  Here's the pool: https://t.co/3VBDWamotJ
	  
	  Let me emphasize: THIS IS NOT AUDITED. USE ONLY AT YOUR OWN RISK. THIS CONTRACT IS EXPERIMENTAL. ([View Tweet](https://twitter.com/ohmzeus/status/1452765688683274242))
	- Looking forward to exploring this more with all of you 
	  
	  p.s. no token rn sorry ([View Tweet](https://twitter.com/ohmzeus/status/1452765690973368321))
	- this link works https://t.co/rI0ZhxPyrQ ([View Tweet](https://twitter.com/ohmzeus/status/1452780099686879233))