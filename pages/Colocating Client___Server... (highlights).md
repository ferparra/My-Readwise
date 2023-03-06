title:: Colocating Client/Server... (highlights)
author:: [[@mhevery on Twitter]]
full-title:: "Colocating Client/Server..."
category:: #tweets
url:: https://twitter.com/mhevery/status/1630413469139996672

- Highlights first synced by [[Readwise]] [[Mar 6th, 2023]]
	- Colocating client/server code in a single file is the next battleground for better DX between meta frameworks.
	  
	  Let's zoom into what it is!
	  
	  🧵🪡🧶 
	  
	  ![](https://pbs.twimg.com/media/FqBkZ3laYAA-sSF.jpg) ([View Tweet](https://twitter.com/mhevery/status/1630413469139996672))
		- **Note**: Thread
	- Module extraction is the way it is done today.
	  1) Well-known top-level function invoked by the server but tree-shaken by the bundler for the client.
	  2) Some form of manual type safety.
	  
	  (no special code transformation needed) 
	  
	  ![](https://pbs.twimg.com/media/FqBkanoaEAAfgHu.jpg) ([View Tweet](https://twitter.com/mhevery/status/1630413505903087617))
	- Function Extraction requires code transformation, which can extract inlined functions into top-level exports (module extraction)
	  
	  Advantage:
	- Closure Extraction (similar to function extraction, but) can also capture closure variables. 🤯
	  
	  Advantages: