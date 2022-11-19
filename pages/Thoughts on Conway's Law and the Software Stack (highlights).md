title:: Thoughts on Conway's Law and the Software Stack (highlights)
author:: [[blog.jessfraz.com]]
full-title:: "Thoughts on Conway's Law and the Software Stack"
category:: #articles
url:: https://blog.jessfraz.com/post/thoughts-on-conways-law-and-the-software-stack/

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- “organizations which design systems … are constrained
	  to produce designs which are copies of the communication structures of these
	  organizations.”
	- Speculative execution was
	  a feature intended to make processors faster but was never thought about in
	  terms of the vector of hacking something running multi-tenant compute,
	  like a cloud provider. Seems like the software and hardware layers should
	  better communicate…
	- A common miscommunication is the “window dressing.” For example, there is a
	  feature in kubernetes that prevents exec-ing into
	  containers. This is implemented by merely preventing the
	  API call in kubernetes. If a person has access to a cluster there are about 4 dozen different
	  ways I can think of to exec into a container and bypass this “feature” and
	  kubernetes entirely. Using
	  said “security feature” in kubernetes alone is not sufficient for security in any respect.
	  This is a common pattern.
	- “take the long view, not just the broad view.” We should do this more often
	  when building systems.
		- **Tags**: #[[favorite]]