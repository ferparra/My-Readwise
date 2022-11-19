title:: While Uniswap Advertises... (highlights)
author:: [[@bantg on Twitter]]
full-title:: "While Uniswap Advertises..."
category:: #tweets
url:: https://twitter.com/bantg/status/1455151835828867079

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- While Uniswap advertises their oracles as TWAP, they are actually TWAT (time-weighted average tick). The logarithmic nature of ticks works very differently from the linear nature of prices. While they protect from flash loans, they are much more susceptible to manipulation.
	  
	  1/2 
	  
	  ![](https://pbs.twimg.com/media/FDG0SOPXIAMQ5WM.jpg) ([View Tweet](https://twitter.com/bantg/status/1455151835828867079))
		- **Note**: Thread
	- This chart shows a moment where DUCK/WETH@1% went to zero. Surprisingly, its 30-minute oracle went to zero a minute after, which resulted in a liquidation of @unitprotocol team CDP. Added a simulated TWAP to show the stark the difference between the ticks and the price.
	  
	  2/2 ([View Tweet](https://twitter.com/bantg/status/1455151838232186888))