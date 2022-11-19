title:: Swapchains and Frame Pacing (highlights)
author:: [[raphlinus.github.io]]
full-title:: "Swapchains and Frame Pacing"
category:: #articles
url:: https://raphlinus.github.io/ui/graphics/gpu/2021/10/22/swapchain-frame-pacing.html

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Graphics performance is a tradeoff between throughput, latency, and power, with smoothness sometimes also a consideration
	- The standard solution is double buffering. One buffer is designated the “front buffer,” and video scanout occurs from that. The other buffer is the “back buffer,” and it is free for the application to scribble on. Once painting is complete, the app swaps the two buffers, the front buffer becoming back and vice versa, so scanout occurs from the current front buffer.