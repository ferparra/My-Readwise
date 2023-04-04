title:: 1/ Many of You Have Aske... (highlights)
author:: [[@chameleon_jeff on Twitter]]
full-title:: "1/ Many of You Have Aske..."
category:: #tweets
url:: https://twitter.com/chameleon_jeff/status/1642198518319452160

- Highlights first synced by [[Readwise]] [[Apr 2nd, 2023]]
	- 1/ Many of you have asked for specific latency tricks on different exchanges, since infrastructure optimization is the foundation of a profitable crypto HFT strategy.
	  
	  Here are some lesser known insights: filtering retail flow on Upbit and bypassing the risk engine on Binance  🧵 ([View Tweet](https://twitter.com/chameleon_jeff/status/1642198518319452160))
		- **Note**: Thread
	- 2/ First up is the counterparty feed trick on Upbit. It's my favorite way to understand autocorrelated retail flow.
	  
	  Though this trick is not technically related to decreasing latency, it comes from a similar source of deeply understanding the exchange technology stack. ([View Tweet](https://twitter.com/chameleon_jeff/status/1642198520982814720))
	- 3/ Upbit labels trades with "sequential_id". The last two digits of this number are the fee tiers of the maker and taker respectively.
	  
	  Fee tiers are strongly correlated with sophistication of the account. And as we know, retail flow is one of the best inputs for quant signals. https://t.co/1AFt1mvCGy ([View Tweet](https://twitter.com/chameleon_jeff/status/1642198523591655426))
	- 4/ Up next, the Binance futures non-liquidation flag for order entry.
	  
	  This setting allows you to bypass the liquidation engine altogether. Set "nl": true in the order JSON you send and the order gets routed straight to the matching engine, shaving a few ms off round trip latency ([View Tweet](https://twitter.com/chameleon_jeff/status/1642198526414446592))
	- 5/ There's an agreement between exchange and API user to not abuse this feature, so obviously make sure you are running a profitable, high sharpe strategy.
	  
	  The non-liquidation flag is understandably not documented, because if abused the exchange could become insolvent. ([View Tweet](https://twitter.com/chameleon_jeff/status/1642198529035882500))
	- 6/ However, for HFT as long as you do the margin checks on your side, saving this latency on server-side risk checks can drastically improve your place in queue and improve your fill rate.
	  
	  Of course, measure for your own infra setup before using. ([View Tweet](https://twitter.com/chameleon_jeff/status/1642198531619569665))
	- 7/ Hope these tips were helpful for people. The devil is in the details with crypto HFT, and it's important to understand all the little details that could be setting back an otherwise profitable strategy. Let me know how they work on your live trading systems. 
	  
	  ![](https://pbs.twimg.com/media/FspC3graAAAisBF.jpg) ([View Tweet](https://twitter.com/chameleon_jeff/status/1642198541945937921))