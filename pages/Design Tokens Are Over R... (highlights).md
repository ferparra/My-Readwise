title:: Design Tokens Are Over R... (highlights)
author:: [[@NateBaldwinArt on Twitter]]
full-title:: "Design Tokens Are Over R..."
category:: #tweets
url:: https://twitter.com/NateBaldwinArt/status/1590186014769033218

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Design tokens are over reduced when approached as merely “json data” or key-value pairs. 
	  
	  It’s a 🧵
	  #designtokens ([View Tweet](https://twitter.com/NateBaldwinArt/status/1590186014769033218))
		- **Note**: Thread
	- Tokens encapsulate a ✨concept✨ take the concept of a “link color”— initially you may think, easy, linkColor: $color300
	  But… ([View Tweet](https://twitter.com/NateBaldwinArt/status/1590186015805050882))
	- Then you also support dark mode. Like many others, you choose $color600 as a “dark mode alternative” ([View Tweet](https://twitter.com/NateBaldwinArt/status/1590186017369518081))
	- This is a simple use case, BUT now what do you do if you support increased contrast mode? In light mode this may be $color200; dark mode $color500. 
	  But wait…. ([View Tweet](https://twitter.com/NateBaldwinArt/status/1590186018464215040))
	- The prefers-contrast query also supports LESS contrast, so for linkColor this may be $color400 in light; $color700 in dark.
	  
	  Already getting complex. There’s multiple dimensions to this concept already, but… ([View Tweet](https://twitter.com/NateBaldwinArt/status/1590186019831545858))
	- Windows high contrast mode support would require a different value altogether: “linktext”— the windows keyword to ensure links update to user-specified color. ([View Tweet](https://twitter.com/NateBaldwinArt/status/1590186020972433410))
	- The concept seems simple: it’s just the color for links.
	  
	  But it’s ✨multidimensional✨, and conditional on systemwide variables. ([View Tweet](https://twitter.com/NateBaldwinArt/status/1590186022029381633))
	- I believe storing tokens in a type of semantic data model, or NoSQL database format that allows for this ✨flexibility✨ is the future of design tokens. ([View Tweet](https://twitter.com/NateBaldwinArt/status/1590186023409324035))