title:: I Had a Ton of Fun Build... (highlights)
author:: [[@emilkowalski_ on Twitter]]
full-title:: "I Had a Ton of Fun Build..."
category:: #tweets
url:: https://twitter.com/emilkowalski_/status/1498659355377344514

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- I had a ton of fun building the command menu @Compound and thought I'd share some technical details about it 🧵 
	  
	  ![](https://pbs.twimg.com/media/FMxOu74UYAEoVnP.jpg) ([View Tweet](https://twitter.com/emilkowalski_/status/1498659355377344514))
		- **Note**: Thread
	- Clients expect quick and complete search results. To facilitate this, we used Fuse.js and Algolia. 
	  Fuse.js searches locally while Algolia combs through 22K+ institutions in under 10ms on the server and ranks results based on internal metrics such as usage and health rate. https://t.co/1mMMVIRU8V ([View Tweet](https://twitter.com/emilkowalski_/status/1498659418694557700))
	- Oftentimes, a user isn't going to enter the exact search term associated with the account or institution they want to add.
	  
	  To solve for this, we augmented our indexes with extra identifiers so that users can find Carta when they search “RSU” or Ethereum when querying for “NFT” ([View Tweet](https://twitter.com/emilkowalski_/status/1498659422310043648))