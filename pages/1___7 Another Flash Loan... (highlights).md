title:: 1/7 Another Flash Loan... (highlights)
author:: [[@FrankResearcher on Twitter]]
full-title:: "1/7 Another Flash Loan..."
category:: #tweets
url:: https://twitter.com/FrankResearcher/status/1398114970508877829

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- 1/7
	  
	  Another flash loan attack on a major DeFi protocol on BSC. 
	  
	  Today $7.2M was stolen from @burger_swap in 14 transactions.
	  
	  Let’s see what’s happened👇 
	  
	  ![](https://pbs.twimg.com/media/E2cXPh0XEAEgiGk.jpg) ([View Tweet](https://twitter.com/FrankResearcher/status/1398114924337971201))
		- **Note**: Thread
	- 2/7
	  
	  What was stolen:
	- 3/7
	  
	  Each attack looked like this (using the example of the WBNB pool):
	  
	  1) Flash swap 6k WBNB ($2M) from PancakeSwap
	  
	  2) Swap almost all WBNB to 92k BURGER on BurgerSwap 
	  
	  ![](https://pbs.twimg.com/media/E2cXbYwWEAELfI4.jpg) ([View Tweet](https://twitter.com/FrankResearcher/status/1398114938472865792))
	- 4/7
	  
	  3) Create pair with a fake token on BurgerSwap and add 100 fake tokens and 45k BURGER
	  
	  4) Swap 100 fake tokens to 4.4k WBNB through the pool from the third step
	  
	  5) Because of reentrancy in time of transfer fake token attacker did another swap from 45k BURGER to 4.4k WBNB 
	  
	  ![](https://pbs.twimg.com/media/E2caIZgWYAASoI6.jpg) ([View Tweet](https://twitter.com/FrankResearcher/status/1398114953513648129))
	- 5/7
	  
	  6) In total attacker received 8.8k WBNB for the two latest steps
	  
	  7) Swap 493 WBNB to 108.7k BURGER on BurgerSwap
	  
	  8) Repay flash swap 
	  
	  ![](https://pbs.twimg.com/media/E2cZqk0XEAAt4qm.jpg) ([View Tweet](https://twitter.com/FrankResearcher/status/1398114958919995398))
	- 6/7 
	  
	  The exploit happened because the attacker could do reentrance and did a second swap before reserves, which are used to calculate the number of tokens in swaps, were updated. 
	  
	  ![](https://pbs.twimg.com/media/E2cZ-foX0AEW5WV.jpg) ([View Tweet](https://twitter.com/FrankResearcher/status/1398114964557152257))
	- 7/7
	  
	  The stolen funds are still being sold and withdrawn to Ethereum via the Nerve bridge.
	  
	  There are about $1.7M left on BSC in BURGER and xBURGER.
	  
	  On Ethereum, there are 1.4k ETH ($3.8M) and 1M DAI. 
	  
	  ![](https://pbs.twimg.com/media/E2caFEOX0AMuQ3V.jpg) ([View Tweet](https://twitter.com/FrankResearcher/status/1398114970508877829))