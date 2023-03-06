title:: Stack Overflow Is a Mult... (highlights)
author:: [[@sahnlam on Twitter]]
full-title:: "Stack Overflow Is a Mult..."
category:: #tweets
url:: https://twitter.com/sahnlam/status/1629713954225405952

- Highlights first synced by [[Readwise]] [[Feb 28th, 2023]]
	- Stack Overflow is a multi-tenant monolithic application serving 2 billion monthly page views across 200 sites.
	  
	  Here are some amazing stats: 
	  
	  ![](https://pbs.twimg.com/media/Fp3oMoqacAEqah1.jpg) ([View Tweet](https://twitter.com/sahnlam/status/1629713954225405952))
		- **Note**: Thread
	- It's on-prem, with only nine IIS web servers.
	  
	  Each server runs their highly optimized .NET code, handling 6000 rps each, and consuming only 5 - 10% capacity.
	  
	  The code minimizes memory allocation to keep garbage collection infrequent. ([View Tweet](https://twitter.com/sahnlam/status/1629713959313088514))
	- SQL Server has 1.5TB of RAM with no caching layer.
	  
	  That is a third of the entire Q&A dataset.
	  
	  Caching didn't work due to the wide distribution of questions. Most cached items expired unused.
	  
	  Removed Redis 4 years ago; average latency remained unchanged at 20ms. ([View Tweet](https://twitter.com/sahnlam/status/1629713961951330304))
	- Reference:
	  [1] Podcast: https://t.co/opTLu4OWbx
	  [2] https://t.co/90lKwqTjOG ([View Tweet](https://twitter.com/sahnlam/status/1629713964564348928))
	- Like/Retweet the first tweet to share the learning: https://t.co/ueHFWXDual ([View Tweet](https://twitter.com/sahnlam/status/1629713967135457284))