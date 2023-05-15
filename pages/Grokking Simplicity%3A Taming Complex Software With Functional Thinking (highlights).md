title:: Grokking Simplicity: Taming Complex Software With Functional Thinking (highlights)
author:: [[Eric Normand]]
full-title:: "Grokking Simplicity: Taming Complex Software With Functional Thinking"
category:: #articles
url:: https://bagerbach.com/books/grokking-simplicity

- Highlights first synced by [[Readwise]] [[May 2nd, 2023]]
	- Functional programming is a programming paradigm that uses mathematical functions & aims to avoid side effects by using pure functions. ([View Highlight](https://read.readwise.io/read/01gzcmdaxrjwhxy1vadchabcxc))
	- **Pure functions** are functions that only depend on their arguments and have no side effects. ([View Highlight](https://read.readwise.io/read/01gzcmdnfs2ws95s2vmpvffm1s))
	- In stratified design, each layer builds on those beneath it.
	  
	  Towards the top layers, changes occur frequently. Towards the bottom layers, changes are seldom. The main layers are business rules (top) → domain rules (mid) → tech stack (bot). ([View Highlight](https://read.readwise.io/read/01gzcme86v3bsnf6xa7msh5w4p))
	- Copy-on-write
	  
	  Implementing copy-on-write operations can help with immutability. ([View Highlight](https://read.readwise.io/read/01gzcmemr6zq1zp3w5s6xzcwc6))
	- **The idea behind all this:** turning writes to reads - and reads to immutable data structures are calculations. ([View Highlight](https://read.readwise.io/read/01gzcmeznvd6z1yfbwvgmb8r5e))
	- **Why the reactive architecture is good**
	  
	  1.  Decouples cause and effect; by using the observer pattern, you don't have to call various elements where they don't belong.
	  2.  Treats steps as pipelines. Data flows naturally through, like with promises in JS. There are frameworks that can help, e.g. RxJs.
	  3.  Creates timeline flexibility (if desired). The timelines are shorter, and there are no shared resources between them. This prevents many common issues, e.g. race conditions, etc. ([View Highlight](https://read.readwise.io/read/01gzcmhjye2r67mtr2s2qfzpp7))