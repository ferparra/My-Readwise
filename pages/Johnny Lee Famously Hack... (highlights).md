title:: Johnny Lee Famously Hack... (highlights)
author:: [[@StrangeNative on Twitter]]
full-title:: "Johnny Lee Famously Hack..."
category:: #tweets
url:: https://twitter.com/StrangeNative/status/1631350356058726411

- Highlights first synced by [[Readwise]] [[Mar 6th, 2023]]
	- Johnny Lee famously hacked a Wii Remote to turn a 2D screen into a 3D window. We revived this trick in Chrome using a standard webcam.
	  
	  Here’s how we did it. 🧵👇 https://t.co/lcKybr3pZD ([View Tweet](https://twitter.com/StrangeNative/status/1631350356058726411))
		- **Note**: Thread
	- We send the webcam video through Google’s MediaPipe Face Mesh library to track our eyes. https://t.co/Wl0SYYEcr1 ([View Tweet](https://twitter.com/StrangeNative/status/1631350361830088716))
	- We transformed the monitor into a virtual window by recreating the real world in our game engine with precise dimensions. The webcam is the origin of the world, and the virtual window has the exact same dimensions as the screen. https://t.co/wpt5qotzlz ([View Tweet](https://twitter.com/StrangeNative/status/1631350365705891841))
	- We place a virtual camera at the position of the right eye, and use off-axis perspective projection to render what the eye sees. https://t.co/lqbFtFueyF ([View Tweet](https://twitter.com/StrangeNative/status/1631350370227343360))
	- A normal (on-axis) perspective projection doesn’t work — you end up seeing past the edges of the virtual window. https://t.co/f6qMDElqMd ([View Tweet](https://twitter.com/StrangeNative/status/1631350373943504896))
	- Anything behind the virtual window appears to have depth, and anything in front of it appears to pop out of the screen. The illusion truly shines when you close one eye. https://t.co/sC0yCQdpYt ([View Tweet](https://twitter.com/StrangeNative/status/1631350377311514625))
	- Check out our new repo for a more in-depth breakdown: https://t.co/XkcF3I5rKC https://t.co/L4alJzz4Yj ([View Tweet](https://twitter.com/StrangeNative/status/1631350380939595776))