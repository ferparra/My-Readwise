title:: Coping With Nontermination: Some Thoughts on Stopping Loops (highlights)
author:: [[outerproduct.net]]
full-title:: "Coping With Nontermination: Some Thoughts on Stopping Loops"
category:: #articles
url:: https://outerproduct.net/boring/2023-02-11_term-loop.html
tags:: #[[computer science]] #[[functional programming]]

- Highlights first synced by [[Readwise]] [[Apr 7th, 2023]]
	- considered desirable that a compiler be able to eliminate side-effect-free loops with no data dependents, even if those loops were potentially non-terminating. ([View Highlight](https://read.readwise.io/read/01gx2271d9y66gnexpkrwdpdhz))
	- Lattices
	  
	  One option, quite boring, is to consider potential non-termination a side effect. That would be like putting up a great blinder in front of every loop until or unless we can prove whether it terminates; probably crudely effective, but we can do better. In order to create a [combining analysis that fits into a monotone analysis framework](https://scholarship.rice.edu/bitstream/handle/1911/96451/TR95-252.pdf), we’ll associate with each of our terms a *halting* type telling whether that term halts or not. This type belongs to a straightforward lattice which will start off with just four elements: *halts*(⊥) (an identity that means whatever we want it to); *halts*(*true*) (does halt); *halts*(*false*) (doesn’t halt); and *halts*(⊤) (don’t know), in the obvious arrangement. ([View Highlight](https://read.readwise.io/read/01gx226hnyhfw7xxetqjm64k7w))
		- **Note**: Halting type associated with terms creates lattice.