title:: I've Seen Microfrontends... (highlights)
author:: [[@housecor on Twitter]]
full-title:: "I've Seen Microfrontends..."
category:: #tweets
url:: https://twitter.com/housecor/status/1139494356174417920

- Highlights first synced by [[Readwise]] [[Mar 31st, 2023]]
	- I've seen microfrontends work well with these rules:
	  1. Consistent tech. All microfrontends use the same JS lib (e.g. React)
	  
	  2. Each team shares *dumb* components (accept all dependencies via props)
	  
	  3. Load shared dependencies (React, Router, etc) via CDN ([View Tweet](https://twitter.com/housecor/status/1139494356174417920))
		- **Note**: Thread
	- These 3 constraints avoid the obvious UX downsides. The user doesn't needlessly download redundant JS libs as they navigate the app. The app container is responsible for all API calls, so redundant calls aren't an issue. And *dumb* components are easy to compose, test, and reuse. ([View Tweet](https://twitter.com/housecor/status/1139495013598076928))
	- That said, with these constraints, one could argue this isn't the microfrontends pattern. ¯\_(ツ)_/¯.
	  
	  To me, there's a spectrum here to consider. Full team independence hurts user experience (UX). These constraints slightly reduce developer experience (DX) to help improve UX. ([View Tweet](https://twitter.com/housecor/status/1139496454387634176))
	- And for those who haven't read it already, here's a solid overview of the microfrontends pattern: https://t.co/ADxbWetRJW
	  
	  I think of this like discussing government. The article describes near full anarchy. Each team for itself. I think wisdom lies in thoughtful collaboration. ([View Tweet](https://twitter.com/housecor/status/1139497234347831301))
	- Here's how I see the spectrum. The Microfrontend pattern that has people concerned is total independence. I've seen the pattern work when you soften it a bit with strategic collaboration between teams. Doing so mitigates the downsides. 
	  
	  ![](https://pbs.twimg.com/media/D9BVRAxX4B8NiKs.jpg) ([View Tweet](https://twitter.com/housecor/status/1139504822930092033))