title:: Did You Know: 🤔 The Inf... (highlights)
author:: [[@matthughson on Twitter]]
full-title:: "Did You Know: 🤔 The Inf..."
category:: #tweets
url:: https://twitter.com/matthughson/status/1605346030505308160

- Highlights first synced by [[Readwise]] [[Dec 23rd, 2022]]
	- Did you know: 🤔
	  
	  The infamous "sprite flicker" you see on the NES, is not actually a built-in hardware feature.
	  
	  This flicker needed to be hand-coded into every game!  
	  
	  But why!? 🧵👇 https://t.co/L6EcmSgMCl ([View Tweet](https://twitter.com/matthughson/status/1605346030505308160))
		- **Note**: Thread
	- The flicker is an attempt to avoid a limitation of the NES: 
	  
	  The NES can only display 8 sprites per horizontal line of the screen.
	  
	  Source: https://t.co/4BgUCbw8hl https://t.co/Tpw04pR07H ([View Tweet](https://twitter.com/matthughson/status/1605346039334305792))
	- The NES's default behavior is to *stop drawing sprites* once that 8 sprite limit it reached. This is what *that* looks like. 
	  
	  Notice that the purple character on the left just completely vanishes. You can imagine why games avoided this. 
	  
	  (The 4 skeletons use 8 sprites total) https://t.co/sRQeccaV1u ([View Tweet](https://twitter.com/matthughson/status/1605346054593183744))
	- Here's a basic version of the flicker. In an emulator you can see that the sprite memory on the right (highlighted with a red circle) is changing the order of sprite data every frame, which means that *which* sprites come *after* the 8-sprite-limit changes every frame aka flicker https://t.co/w1GTj3c8cJ ([View Tweet](https://twitter.com/matthughson/status/1605346079528349696))
	- And the final results running on a real NES + a CRT TV where I find it looks a lot better than in an emulator + LCD. #nesdev https://t.co/MJtL3RSp0o ([View Tweet](https://twitter.com/matthughson/status/1605346665514557440))
	- @RistarGameREAL @bmusic242 @Archanea_ They do a lot of very fast animations that blend together to create the illusion of more sprites then there actually are, especially for the powers. https://t.co/eJwO4RrVns ([View Tweet](https://twitter.com/matthughson/status/1606046350449278978))