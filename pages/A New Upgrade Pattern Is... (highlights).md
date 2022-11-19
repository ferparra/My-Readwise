title:: A New Upgrade Pattern Is... (highlights)
author:: [[@smpalladino on Twitter]]
full-title:: "A New Upgrade Pattern Is..."
category:: #tweets
url:: https://twitter.com/smpalladino/status/1389939169821184001

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- A new upgrade pattern is available in @OpenZeppelin Contracts 4.1! Welcome UUPS proxies to the family.
	  
	  @frangio_ has put together an awesome tutorial in the forum, but let's go through the differences here in a 🧵
	  
	  https://t.co/dX5dcTstLb ([View Tweet](https://twitter.com/smpalladino/status/1389939156525232130))
		- **Note**: Thread
	- The proxies that historically shipped with OpenZeppelin tools were Transparent proxies. 
	  
	  https://t.co/lh4KSLsIDr
	  
	  These delegatecall-based proxies also contain the logic for executing upgrades and managing ownership. ([View Tweet](https://twitter.com/smpalladino/status/1389939158383271940))
	- As such, they have few requirements on the target implementation contract: just use an initializer instead of a constructor and you're good to go!
	  
	  On the other hand, they are more expensive to deploy (more code in the proxy itself!) and require two SLOADs per delegated call. ([View Tweet](https://twitter.com/smpalladino/status/1389939160941740035))
	- The two SLOADs were not a big deal at the time, but after two hard forks (Istanbul and Berlin) repricing them, we need to drive down their cost as much as possible.
	  
	  And that's where UUPS proxies come in! ([View Tweet](https://twitter.com/smpalladino/status/1389939163290652677))
	- UUPS proxies are a lot simpler than Transparent, and they only have the logic for delegating the call. This makes them much cheaper to deploy, and each all has half the overhead (just a single SLOAD).
	  
	  https://t.co/tR4MDy1CfM
	  
	  But this puts more burden on the implementation. ([View Tweet](https://twitter.com/smpalladino/status/1389939166109212675))
	- UUPS proxies require that the implementation contract has the logic for executing the upgrade itself. This requires extending from a base UUPSUpgradeable contract:
	  
	  https://t.co/OzTKJnsynW
	  
	  And the upgrade plugins will notify you if you forget to include it! ([View Tweet](https://twitter.com/smpalladino/status/1389939167988228096))
	- Also, keep in mind we also have Beacon proxies in the Contracts library, which are tailored for the use case of having multiple copies of the same contract that need to be upgraded simultaneously.
	  
	  https://t.co/BJGoiNLuRe ([View Tweet](https://twitter.com/smpalladino/status/1389939169821184001))