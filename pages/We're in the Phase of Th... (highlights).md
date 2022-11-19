title:: We're in the Phase of Th... (highlights)
author:: [[@n2ckchong on Twitter]]
full-title:: "We're in the Phase of Th..."
category:: #tweets
url:: https://twitter.com/n2ckchong/status/1383233342649225216

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- We're in the phase of the market where there's a lot of retail inbounds but not enough education about the Ethereum ecosystem and DeFi.
	  
	  So, let's break down the basics of some of the top protocols.
	  
	  First on deck: Aave (@AaveAave), an Ethereum-based money market protocol.
	  
	  A 🧵 https://t.co/DJV0B1hDLi ([View Tweet](https://twitter.com/n2ckchong/status/1383233304892117005))
	- TL;DR: Aave is a protocol through which any user anywhere in the world can take decentralized loans by collateralizing their assets. 
	  
	  Aave also allows those will idle assets to earn a relatively safe return on capital from lenders, whose rates are determined by a curve. ([View Tweet](https://twitter.com/n2ckchong/status/1383233306553053190))
	- 1/ For years, most crypto assets had no indirect or direct utility.
	  
	  Users would hold BTC, ETH, and other assets (including many ERC-20 tokens) with no expectation of a native yield or dividends. 
	  
	  ETH, for instance, was long just an asset for transaction fees, as was Bitcoin. ([View Tweet](https://twitter.com/n2ckchong/status/1383233307639308292))
	- 2/ If users wanted to borrow against their assets, they were relegated to centralized platforms—which were few and far between years ago. ([View Tweet](https://twitter.com/n2ckchong/status/1383233308708904963))
	- 3/ Aave, formerly ETHLend, is a protocol allowing users the ability to lend and borrow on-chain, without KYC and untransparent fees.
	  
	  Users can deposit a variety of assets as collateral, then use that collateral as ammo to borrow other assets to be used in DeFi or beyond. ([View Tweet](https://twitter.com/n2ckchong/status/1383233309686210560))
	- 4/ Today, Aave supports a handful of Ethereum-based assets, including but not limited to stablecoins (USDC, DAI, USDT), Ethereum itself, DeFi blue chips (UNI, YFI, SNX), Wrapped Bitcoin, and a number of other assets. 
	  
	  Loans are *overcollateralized*. ([View Tweet](https://twitter.com/n2ckchong/status/1383233310722195456))
	- 5/ There are two core buckets of users of Aave: 
	  
	  1. Those looking for steady, relatively safe yield on idle assets.
	  
	  2. Those that want to leverage their assets by borrowing against their holdings, then trading and spending the loan to achieve utility beyond the rate they pay. ([View Tweet](https://twitter.com/n2ckchong/status/1383233311829495810))
	- 6/ For those in the first bucket, the user flow is:
	- 7/ For those in the second bucket, the user flow is:
	- 8/ There are a few use cases with borrowing on-chain. Let's explain a few.
	  
	  Shorting:
	  
	  A user can borrow an asset from Aave, sell it, buy it back when the price is lower, then pocket the delta.
	  
	  This works because the loan is denominated in the asset(s) borrowed. ([View Tweet](https://twitter.com/n2ckchong/status/1383233316921384965))
	- 9/ Earning a yield on any asset:
	  
	  ETH natively does not produce yield.
	  
	  It can be used as collateral to borrow assets that *can* earn yield.
	  
	  Assuming you can earn 15% on USDC and borrow @ 5%, borrowing USDC at a 200% collat. ratio will allow for an effective yield of 5% on ETH. ([View Tweet](https://twitter.com/n2ckchong/status/1383233317919547399))
	- 10/ Spending:
	  
	  Say a user is holding Wrapped Bitcoin and wants something on-chain or IRL, though doesn't want to get rid of their WBTC exposure.
	  
	  A user can collateralize their WBTC, buy what they want, then pay back the loan with income or other assets to reclaim their WBTC. ([View Tweet](https://twitter.com/n2ckchong/status/1383233318968193030))
	- 11/ Now that we have some use cases out of the way, let's take a look at flash loans. 
	  
	  Aave pioneered flash loans, a concept where anyone can borrow any amount of capital within a single block for a number of use cases.
	  
	  Did a thread here in the past.
	  
	  https://t.co/FRn5Pj2TFk ([View Tweet](https://twitter.com/n2ckchong/status/1383233320046133251))
	- 12/ Due to inefficiencies in the market, users can borrow large chunks of capital from Aave within a block, to balance the price of assets between different exchanges, along with other use cases. https://t.co/HixdJyH5sI ([View Tweet](https://twitter.com/n2ckchong/status/1383233322977878017))
	- In the above transaction:
	- 13/ Now, a look at a few of the mechanics of the protocol to help contextualize how Aave works.
	  
	  I'll cover:
	- 14/ Interest rates: Aave's rates on the lender and borrower sides are determined by a curve.
	  
	  The more an asset is utilized, the higher the rate lenders earn and borrowers pay. 
	  
	  The borrow rate is always above the deposit rate. 
	  
	  Here's the borrow rate model for USDC / USDT. https://t.co/4zFeLWeBGf ([View Tweet](https://twitter.com/n2ckchong/status/1383233328363368456))
	- 15/ Aave has the added component of a "stable" borrowing rate.
	  
	  To mitigate unexpected spikes in utilization affecting the rate one pays on their loan, users can lock in a fixed rate, so they can manage risk properly.
	  
	  This rate can readjust based on market conditions. ([View Tweet](https://twitter.com/n2ckchong/status/1383233330015969284))
	- 16/ Terms: 
	  
	  Aave has a number of loan terms that dictate how much one can borrow, at what point they are liquidated, and how much they pay when they are liquidated.
	  
	  These terms are determined by a risk team, who assess market conditions to minimize risk to protocol collateral. ([View Tweet](https://twitter.com/n2ckchong/status/1383233331102289926))
	- 17/ Liquidations:
	  
	  Unlike traditional loans, Aave loans are liquidated autonomously when a user's loan-to-value ratio falls below certain values.
	  
	  A large enough drop in the value of one's collateral will allow users to bid the collateral, sell it, then pocket a bonus. https://t.co/uzd2bQb87K ([View Tweet](https://twitter.com/n2ckchong/status/1383233333505650689))
	- 18/ aTokens: Users that deposit assets into Aave are granted an aToken representing their deposit (USDC -> aUSDC).
	  
	  aTokens are yield-bearing assets that accrue interest in real time, allowing one to watch their deposited assets grow by block. ([View Tweet](https://twitter.com/n2ckchong/status/1383233334927532037))
	- 19/ These basics aside, Aave, at the end of the day, is a core money lego.
	  
	  It can be used by other developers to build interesting applications and use cases.
	  
	  For instance... ([View Tweet](https://twitter.com/n2ckchong/status/1383233336164851716))
	- 20/ @BasketDAOOrg: BasketDAO deposits assets under management into Aave, which creates a yield-bearing index
	  
	  @APWineFinance: APWine allows users to trade unrealized yield 
	  
	  etc.
	  
	  aTokens, flash loans, etc. can all be used in tandem with other contracts to create use cases. https://t.co/9YKV8ASyCH ([View Tweet](https://twitter.com/n2ckchong/status/1383233339306348548))
	- Fini/ As always, none of this is investment advice. Please take caution when interacting with protocols on-chain and understand all risks before doing so.
	  
	  As I said at the start of the thread, this is the first of many. 
	  
	  More to come. https://t.co/p6sWXcqroB ([View Tweet](https://twitter.com/n2ckchong/status/1383233342649225216))