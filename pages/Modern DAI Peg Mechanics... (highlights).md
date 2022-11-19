title:: Modern DAI Peg Mechanics... (highlights)
author:: [[@Kurt_M_Barry on Twitter]]
full-title:: "Modern DAI Peg Mechanics..."
category:: #tweets
url:: https://twitter.com/Kurt_M_Barry/status/1429564277329911809

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Modern DAI Peg Mechanics 101
	  
	  I've seen a lot of confusion and questions about how DAI stays at ~$1 market price, particularly since some wrinkles have been added beyond what's in the white paper.
	  
	  So, I figured I'd take a stab at fixing this. If you want to know more, read on! 
	  
	  ![](https://pbs.twimg.com/media/E9a7edhXMAUBgaN.png) ([View Tweet](https://twitter.com/Kurt_M_Barry/status/1429564277329911809))
		- **Note**: Thread
	- Asset pricing really is all about supply and demand.
	  
	  If you want a stable asset, you need to balance supply and demand around the target price for that asset.
	  
	  This is tough, because there are external factors that influence S&D that you can't control. ([View Tweet](https://twitter.com/Kurt_M_Barry/status/1429564279267672067))
	- You need mechanisms that can modulate S&D, and allow effective responses whether DAI is trading above or below the $1 mark.
	  
	  MakerDAO currently has three main tools for _active_ management:
	  1) the Vault mechanism
	  2) the DAI saving rate (DSR)
	  3) the Peg Stability Module (PSM) ([View Tweet](https://twitter.com/Kurt_M_Barry/status/1429564280739872768))
	- 1) Vaults
	  
	  The original core of the protocol--lock a crypto bearer asset, give yourself a DAI loan. Vaults are charged a compounding "stability fee" on their debt. Pricing is done in dollars, and the system treats 1 DAI as $1 in the loan math. 
	  
	  ![](https://pbs.twimg.com/media/E9bEObpXEAAcsFN.jpg) ([View Tweet](https://twitter.com/Kurt_M_Barry/status/1429564284128870400))
	- Liquidation (selling of collateral to recover DAI) occurs if the value of the collateral gets too small compared to the amount borrowed, ensuring at least $1 of value backs each DAI in existence.
	  
	  There's a fairly obvious balancing incentive: ([View Tweet](https://twitter.com/Kurt_M_Barry/status/1429564286146330636))
	- If DAI > $1, it's attractive to mint DAI from a Vault--you get more actual value than the system thinks its crediting you for. This creates supply, which should push price down.
	  
	  If DAI < $1, you can repay your debt at a bargain. This contracts supply, which pushes price up. ([View Tweet](https://twitter.com/Kurt_M_Barry/status/1429564287496884229))
	- However, this arbitrage is not risk-free, there's a lot of friction involved, and it has proven to be a weak effect in practice. Maker governance can modify Vault parameters and even add or remove Vault types to have a stronger effect. ([View Tweet](https://twitter.com/Kurt_M_Barry/status/1429564288826478593))
	- Adding a Vault type opens up new markets for DAI borrowing, boosting supply. Conversely, limiting the amount of DAI that can be created from a Vault type constrains supply. But the various risk parameters, particularly the stability fee, can be used for quicker responses. ([View Tweet](https://twitter.com/Kurt_M_Barry/status/1429564290479140864))
	- Raising fees makes it less attractive to mint DAI, generally limiting supply generation and even contracting it as existing Vaults repay debt.
	  
	  Lowering fees makes minting DAI a better deal, and encourages supply expansion, but only to a point--rates can't go negative. ([View Tweet](https://twitter.com/Kurt_M_Barry/status/1429564292001673222))
	- Governance can tweak other parameters like the collateralization ratios (how much collateral value is required to back each DAI per Vault type) to make DAI minting more or less attractive, but generally fees have the strongest effect. ([View Tweet](https://twitter.com/Kurt_M_Barry/status/1429564293616439306))
	- 2) DAI Savings Rate
	  
	  While the Vault mechanism technically has many adjustable facets, the DSR is very simple: it allows users to lock DAI in a contract to earn a yield (the eponymous "DAI savings rate").
	  
	  The ability to earn yield creates demand for DAI. ([View Tweet](https://twitter.com/Kurt_M_Barry/status/1429564294983790603))
	- Higher yields => more demand, causing the DAI price to rise. Lower yields => less demand, causing the DAI price to fall.
	  
	  An important misconception to avoid is that locking DAI for the DSR reduces supply--it's trivial to tokenize and trade the locked DAI (e.g. the CHAI token). ([View Tweet](https://twitter.com/Kurt_M_Barry/status/1429564296351080457))
	- Rather, the DSR represents a slider for Maker governance to tune DAI demand.
	  
	  You may have picked up on a crucial fact: both stability fees and the DSR need to be lowered to drive DAI creation, but neither one can go sub-zero. If both are zero and still DAI > $1--wat do? ([View Tweet](https://twitter.com/Kurt_M_Barry/status/1429564297693351938))
	- 3. Peg Stability Module
	  
	  That was exactly the corner DAI was backed into in 2020--fees and the DSR were at or near zero, but the market price remained stubbornly above the $1 target.
	  
	  Initially, stablecoin Vaults with low interest rates were tried, but they proved unworkable... ([View Tweet](https://twitter.com/Kurt_M_Barry/status/1429564299060596736))
	- ...because the DAI price remained high, making it impossible to close the arbitrage before fees overwhelmed the initial profit.
	  
	  Enter the Peg Stability Module (PSM), which allows simple exchanges between DAI and other USD-pegged stables (just USDC at first) for a one-time fee. ([View Tweet](https://twitter.com/Kurt_M_Barry/status/1429564300688085002))
	- Suddenly, there was an instant, risk-free arbitrage on the DAI price. Selling USDC for DAI through the PSM creates new DAI (backed by the USDC), expanding supply. Selling of the new supply pushes the price down. Finally, the DAI price normalized to its target. ([View Tweet](https://twitter.com/Kurt_M_Barry/status/1429564302273433605))
	- Nothing comes for free though--there was so much excess demand for DAI beyond what the Vault mechanism could generate that USDC now backs ~60% of DAI. This is rightly a common point of critique, and represents a long-term risk that must be mitigated. 
	  
	  ![](https://pbs.twimg.com/media/E9bPC82XIAIemid.png) ([View Tweet](https://twitter.com/Kurt_M_Barry/status/1429564305381408773))
	- Watch out for near-term evolution like PSMs using different assets to diversify risk, and more DAI generated from off-chain ("real world") assets, as well as new types of crypto-native collateral. ([View Tweet](https://twitter.com/Kurt_M_Barry/status/1429564307193352195))
	- We haven't discussed more passive mechanisms like MKR backstopping of DAI and emergency shutdown--these create assurances regarding the value of DAI, bolstering belief in the $1 target so demand doesn't collapse--but in the interest of time, I'll save those for a 201 thread. ([View Tweet](https://twitter.com/Kurt_M_Barry/status/1429564308883705864))
	- Hopefully that was helpful to someone! Happy to answer any questions here on Twitter, but feel free to swing by the MakerDAO chat or forum any time you like:
	  https://t.co/3kpeGBBLOK
	  https://t.co/qs4v8iZ07d ([View Tweet](https://twitter.com/Kurt_M_Barry/status/1429564310334976008))