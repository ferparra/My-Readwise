title:: Google Has Launched Carb... (highlights)
author:: [[@marktenenholtz on Twitter]]
full-title:: "Google Has Launched Carb..."
category:: #tweets
url:: https://twitter.com/marktenenholtz/status/1551900161386762240

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Google has launched Carbon: a successor to C++.
	  
	  It matches 100% of the performance of C++ and aims to provide a significantly better developer experience.
	  
	  I think this is huge news for ML.
	  
	  Here's why you should care (even if you've never written a line of C/C++ in your life): 
	  
	  ![](https://pbs.twimg.com/media/FYl09_aUYAAAokn.png) 
	  
	  ![](https://pbs.twimg.com/media/FYl0-MfVUAAvPlH.png) ([View Tweet](https://twitter.com/marktenenholtz/status/1551900161386762240))
		- **Note**: Thread
	- (One quick caveat: Carbon is experimental and, well, we all know Google's track record) ([View Tweet](https://twitter.com/marktenenholtz/status/1551900164519931906))
	- Really, there are two main reasons:
	  
	  1. Reducing tech debt in existing libraries
	  2. Making it easier to extend those libraries
	  
	  But first, let's talk about the marriage between Python, C, and machine learning. ([View Tweet](https://twitter.com/marktenenholtz/status/1551900167036514305))
	- There is a *massive* misconception that Python code is ungodly slow for ML tasks.
	  
	  It would actually be true... if nearly all of your code wasn't already running in heavily optimized C libraries. ([View Tweet](https://twitter.com/marktenenholtz/status/1551900169687298050))
	- We can have conversations about whether Python is the future of ML until the cows come home.
	  
	  Personally, I think it probably isn't (unless a fully JIT'd Python clone shows up, which, well... I'm not exactly counting on). ([View Tweet](https://twitter.com/marktenenholtz/status/1551900172187099137))
	- But as it stands now:
	  
	  When you run Python ML code, you're probably looking at maybe a 10% performance overhead?
	  
	  This number is heavily fudged, but I think it's pretty conservative. ([View Tweet](https://twitter.com/marktenenholtz/status/1551900174645047297))
	- Of course, it's only true if we can keep getting developers to write kick-ass C libraries to do all the heavy lifting.
	  
	  Which, of course, brings me to Carbon. ([View Tweet](https://twitter.com/marktenenholtz/status/1551900177224544256))
	- Languages like Rust and Go are fantastic for performance, and we should continue to use them for all kinds of applications.
	  
	  But it's undeniable that we have a vested interest in maintaining the enormous C codebases that make up our favorite ML libraries. ([View Tweet](https://twitter.com/marktenenholtz/status/1551900179745296384))
	- Going by GitHub stats, here's the % of code in C/C++ for some of your favorite libraries:
	  
	  • NumPy: 36.4%
	  • PyTorch: 54.0%
	  • TensorFlow: 62.7%
	  • SciPy: 20.4% (19.1% Fortran)
	  
	  I included the Fortran % for SciPy just to get across how reliant we are on fast library code. ([View Tweet](https://twitter.com/marktenenholtz/status/1551900182224052225))
	- As far as reducing tech debt goes, I really appreciate the pragmatic mission Google has here.
	  
	  It's basically this:
	  
	  • There's a lotta C code out there
	  • That code is great
	  • But it's full of tech debt
	  • Tech debt is inherent to C
	  • More code in C leads to more tech debt ([View Tweet](https://twitter.com/marktenenholtz/status/1551900184828715008))
	- Given that mission, you have 2 options:
	  
	  1. Try to migrate everything off of C
	  2. Extend existing C code with something better
	  
	  1 is a valiant mission, but 2 is more pragmatic in the short term. ([View Tweet](https://twitter.com/marktenenholtz/status/1551900187307544577))
	- (Side note: will CUDA C integrate at all with Carbon? That'd be pretty cool.) ([View Tweet](https://twitter.com/marktenenholtz/status/1551900189761290244))
	- The second major way Carbon could impact ML is by enabling entirely new ML approaches.
	  
	  A tale as old as time in ML: 
	  
	  A new methodology is theorized. It works pretty well, but it's slow and hard to experiment with.
	  
	  Then, someone makes it 1000x faster and it's a game changer. ([View Tweet](https://twitter.com/marktenenholtz/status/1551900192185626624))
	- This was definitely the case with deep learning (when coupled with hardware improvements, at least).
	  
	  I mean, shoot, I even saw AutoARIMA get some big performance boosts recently.
	  
	  How much could we improve GBDT models if we didn't have to write them from scratch in C? ([View Tweet](https://twitter.com/marktenenholtz/status/1551900194748321792))
	- New libraries that are backed by fast, low-level implementations let us Python users try out entirely new methods.
	  
	  Wouldn't it be great if library developers could extend the ocean of ML-focused C to create new libraries for Python users WITHOUT needing to use C? ([View Tweet](https://twitter.com/marktenenholtz/status/1551900197327761413))
	- I don't know if Carbon is going to be ditched in a year or if it's going to revolutionize the way C codebases are maintained.
	  
	  Honestly, the point of this thread is less about Carbon and more about the impact of modern languages. ([View Tweet](https://twitter.com/marktenenholtz/status/1551900199857008641))
	- Here's what I feel pretty confident in saying:
	  
	  User-friendly, batteries-included, low-level languages are going to be immensely impactful in ML in the coming years, and you should keep your eyes out. ([View Tweet](https://twitter.com/marktenenholtz/status/1551900202360905728))
	- TL;DR:
	  
	  1. Python is misunderstood
	  2. But, ML code is still totally reliant on C
	  3. There's an ocean of C code holding ML up
	  4. Carbon could make it much more maintainable
	  
	  Follow me @marktenenholtz for more high-signal ML content! ([View Tweet](https://twitter.com/marktenenholtz/status/1551900204911058944))
	- If you like this content, I go into much more detail on this topic and similar ones in my newsletter.
	  
	  Check it out: https://t.co/34sBfoLpMx ([View Tweet](https://twitter.com/marktenenholtz/status/1551900207415078912))