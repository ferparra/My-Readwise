title:: On a 120Hz Display, Apps... (highlights)
author:: [[@zeddotdev on Twitter]]
full-title:: "On a 120Hz Display, Apps..."
category:: #tweets
url:: https://twitter.com/zeddotdev/status/1633852088433139713

- Highlights first synced by [[Readwise]] [[Mar 10th, 2023]]
	- On a 120Hz display, apps have ~8ms to render each frame without introducing jank. In Electron, this felt impossible to achieve. So to create Zed, we took inspiration from video games and built our own UI framework in Rust that targets modern graphics hardware: GPUI. 🧵... https://t.co/qFDzvG7Wh9 ([View Tweet](https://twitter.com/zeddotdev/status/1633852088433139713))
		- **Note**: Thread
	- Rounded rectangles are a fundamental building block of user interfaces. Zed uses Signed Distance Functions to draw them in parallel entirely on the GPU. https://t.co/KFqehOGa4H ([View Tweet](https://twitter.com/zeddotdev/status/1633852092300312576))
	- Rendering text is equally important. In GPUI, we let the operating system handle font rasterization and cache the resulting pixels into a texture atlas. Glyphs are then read from the atlas and assembled in parallel on the GPU. 
	  
	  ![](https://pbs.twimg.com/media/Fqya0MJWcAAAXWL.jpg) ([View Tweet](https://twitter.com/zeddotdev/status/1633852097039933442))
	- This just scratches the surface of the problems we solved to build GPUI. For more details on how we derived an SDF for rounded rectangles, drew gaussian shadows on the GPU and performed element layout efficiently, check out the blog post!
	  
	  https://t.co/SMkAIxqb5l ([View Tweet](https://twitter.com/zeddotdev/status/1633852101376999425))