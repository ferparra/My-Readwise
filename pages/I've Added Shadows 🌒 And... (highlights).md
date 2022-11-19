title:: I've Added Shadows 🌒 And... (highlights)
author:: [[@anastasiaopara on Twitter]]
full-title:: "I've Added Shadows 🌒 And..."
category:: #tweets
url:: https://twitter.com/anastasiaopara/status/1492429686294683653

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- I've added shadows 🌒 and the ability to adjust wall height ✨suddenly the thing feels slightly more real :3
	  
	  I also feel like I've undergone a rite of passage: my first gpu crash and a driver bug 😅🏆
	  
	  #screenshotsaturday #gamedev  #rustlang 🦀 #opengl #bevyengine #procgen https://t.co/iVhX8jb9B6 ([View Tweet](https://twitter.com/anastasiaopara/status/1492429686294683653))
		- **Note**: Thread
	- The shadows use a simple shadow map, and softness is done with PCSS. It was really fascinating to learn about the complexities of something I used to take for granted 😅 I'm looking forward to exploring more rendering 😊 ([View Tweet](https://twitter.com/anastasiaopara/status/1492429689197150210))
	- The dragging of the wall up and down was quite fun to solve: I find a plane tangent to the wall, and intersect it with a ray from the cursor. That intersection tells me precisely how tall the wall should be to match the cursor in screen space. ([View Tweet](https://twitter.com/anastasiaopara/status/1492429690711195649))
	- As usual, many thanks to @h3r2tic for being my rendering mentor 🙇‍♀️ I'd like to promote his shader-prepper crate (https://t.co/IcuQyNBX3y). I use it for `include` files in my glsl shaders, and it was trivial to hook it up to my hot-reloading solution with `hotwatch` ♥ ([View Tweet](https://twitter.com/anastasiaopara/status/1492429692191883267))