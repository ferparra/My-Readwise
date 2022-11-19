title:: I Used to Be Totally In... (highlights)
author:: [[@flybayer on Twitter]]
full-title:: "I Used to Be Totally In..."
category:: #tweets
url:: https://twitter.com/flybayer/status/1252811740384878592

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- I used to be totally in love with DB+GraphQL in-a-box services like @graphcool and @HasuraHQ 
	  
	  But I now intimately understand their limitations. They are AMAZING for spinning up an app very quickly, but that joy soon turns to sorrow once you need advanced functionality. ([View Tweet](https://twitter.com/flybayer/status/1252811735548915718))
		- **Note**: Thread
	- Tightly coupling your GraphQL API to your database schema is severely limiting. For small apps, it’s really nice, but as soon as you need something really serious it falls apart. ([View Tweet](https://twitter.com/flybayer/status/1252811737583112197))
	- Here’s my currrent stance:
	  
	  Use @HasuraHQ for: 
	  Prototypes, tiny/small apps, quickly adding GraphQL to an existing app
	  
	  Everything else:
	  Use something like AWS AppSync or go full custom with Prisma 2 and Nexus ([View Tweet](https://twitter.com/flybayer/status/1252811740384878592))