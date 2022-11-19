title:: Practical Example: Concentrated Liquidity and Capital Efficiency in Uniswap V2 vs V3 (highlights)
author:: [[crocofinance.medium.com]]
full-title:: "Practical Example: Concentrated Liquidity and Capital Efficiency in Uniswap V2 vs V3"
category:: #articles
url:: https://crocofinance.medium.com/practical-example-concentrated-liquidity-and-capital-efficiency-in-uniswap-v2-vs-v3-cfdf64eefb9f

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- Alice and Bob both want to provide liquidity in an ETH/DAI pool on Uniswap v3. They each have $1m. The current price of ETH is 1,500 DAI.Alice decides to deploy her capital across the entire price range (as she would have in Uniswap v2). She deposits 500,000 DAI and 333.33 ETH (worth a total of $1m).Bob instead creates a concentrated position, depositing only within the price range from 1,000 to 2,250. He deposits 91,751 DAI and 61.17 ETH, worth a total of about $183,500. He keeps the other $816,500 himself, investing it however he prefers.While Alice has put down 5.44x as much capital as Bob, they earn the same amount of fees, as long as the ETH/DAI price stays within the 1,000 to 2,250 range.
	- If Alice deposits $1m worth of liquidity into ETH/DAI = (0; ∞) price range (default Uniswap v2 range), how much assets does Bob have to deposit into the (1000; 2250) price range so that he earns the same fees as Alice as long as the price stays within the specified range?