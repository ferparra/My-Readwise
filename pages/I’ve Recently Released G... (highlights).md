title:: I’ve Recently Released G... (highlights)
author:: [[@amandaghassaei on Twitter]]
full-title:: "I’ve Recently Released G..."
category:: #tweets
url:: https://twitter.com/amandaghassaei/status/1597959908607295488

- Highlights first synced by [[Readwise]] [[Dec 1st, 2022]]
	- I’ve recently released gpu-io –– a WebGL computing library for real-time physics simulations, particle/agent-based systems, cellular automata, image processing, and general purpose GPU computations.
	  
	  Examples: https://t.co/ricQ98ci8K
	  Code: https://t.co/Q97eyb1xKT
	  
	  More info in 🧵 https://t.co/tyiceQxFim ([View Tweet](https://twitter.com/amandaghassaei/status/1597959908607295488))
		- **Note**: Thread
	- gpu-io makes it easy to build GPU-accelerated applications without worrying about low-level WebGL details and browser inconsistencies.
	  
	  I’m using this as the basis for all of my shader experiments, including the fluid/marbling work I’ve been up to lately:
	  https://t.co/UhZtTxRsBs ([View Tweet](https://twitter.com/amandaghassaei/status/1597959913170685954))
	- gpu-io has built-in helper functions for composing real-time physics simulations –– e.g. for applying boundary conditions, flip-flopping prev/next state buffers, rendering particles, and adding touch interactivity.
	  
	  interactive Physarum (slime mold) sim:
	  https://t.co/41apzKNAXX https://t.co/45bJB9wlMs ([View Tweet](https://twitter.com/amandaghassaei/status/1597959941213794307))
	- gpu-io plays nicely with @threejs –– data can be passed between the two libraries via WebGL textures without ever leaving the GPU.
	  
	  Example: https://t.co/uzyZZMn2iP
	  More info: https://t.co/rP1F8JATbN https://t.co/2c7OXOn0K0 ([View Tweet](https://twitter.com/amandaghassaei/status/1597960786051092480))
	- gpu-io is designed for WebGL 2 with fallbacks to convert your shader code to run in WebGL 1 if needed –– so it should run on practically any mobile or older browser.  You can try all of the examples with WebGL 1 to test:
	  https://t.co/ricQ97U8UC
	  
	  WebGPU support is planned! 
	  
	  ![](https://pbs.twimg.com/media/Fi0ZEzbVUAEPXkd.jpg) ([View Tweet](https://twitter.com/amandaghassaei/status/1597961271822860288))
	- Had fun putting together the example docs for this repo. Here’s a zoomable Julia set fractal demo:
	  https://t.co/k1aoEhCJ3t
	  
	  You can zoom until you run out of float precision to calculate the image. Would be cool to make this infinitely zoom via self-similarity tricks... https://t.co/6NvzuChWF6 ([View Tweet](https://twitter.com/amandaghassaei/status/1597962090492239877))
	- More examples from the slime mold (Physarum) simulation:
	  https://t.co/41apzKNAXX
	  
	  This one is a mix of grid + particle methods –– lots of little agents interacting with an underlying field of chemo-attractants.
	  
	  Inspired by the incredible work of @mxsage:
	  https://t.co/ysjZZXTydp https://t.co/wIxyk6ofqF ([View Tweet](https://twitter.com/amandaghassaei/status/1597963492757483521))
	- Reaction-diffusion system whose behavior depends on two parameters that vary across x and y. Zoom around parameter space to find regions of interest:
	  
	  https://t.co/PnamIpBuIn
	  
	  Most of the dynamic behavior occurs in a small sliver of parameter space, but it's fun to look around! https://t.co/NMy69HyzD7 ([View Tweet](https://twitter.com/amandaghassaei/status/1597964712196853760))