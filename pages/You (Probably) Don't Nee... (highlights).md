title:: You (Probably) Don't Nee... (highlights)
author:: [[@Infoxicador on Twitter]]
full-title:: "You (Probably) Don't Nee..."
category:: #tweets
url:: https://twitter.com/Infoxicador/status/1606382229764116483

- Highlights first synced by [[Readwise]] [[Dec 24th, 2022]]
	- You (probably) don't need Micro-Frontends
	  
	  This is the "Distributed and Decoupled Spectrum" 
	  
	  Make sure that you explore all the other options before trying to implement a fully distributed system 
	  
	  ![](https://pbs.twimg.com/media/FksAD4yWIAA4GZo.jpg) ([View Tweet](https://twitter.com/Infoxicador/status/1606382229764116483))
		- **Note**: Thread
	- Let's start with the Monolith.
	  
	  Either a backend and frontend together or a frontend monolith connecting to APIs.
	  
	  Great for solo devs and small teams. 
	  
	  Monoliths can definitely scale to millions of users ([View Tweet](https://twitter.com/Infoxicador/status/1606382232360390665))
	- The Modular Monolith:
	  
	  You can get clear boundaries, a better-organized app and multiple teams collaborating at the same time.
	  
	  However, the application still has to be deployed as a single unit. ([View Tweet](https://twitter.com/Infoxicador/status/1606382234088480768))
	- Integrated Applications:
	  
	  They could be developed and deployed independently but often there is an integration step at build time where all the pieces come together and get deployed as a single unit. 
	  
	  Monorepos are a great tool for integrated applications. ([View Tweet](https://twitter.com/Infoxicador/status/1606382236156076032))
	- Vertical Micro-Frontends
	  
	  Independently deployable apps that are mounted on a different URL path but under the same domain.
	  
	  Whenever you have to cross an app boundary, the new app is loaded entirely.
	  
	  There is no horizontal composition which could impact performance and UX. ([View Tweet](https://twitter.com/Infoxicador/status/1606382238089838592))
	- Runtime Micro-Frontends.
	  
	  This type allows you to compose vertically and horizontally. The app works and feels like a single unit but is composed of multiple apps at runtime.
	  
	  There is no full page refresh, the perfect balance of UX and DX. ([View Tweet](https://twitter.com/Infoxicador/status/1606382240837079055))