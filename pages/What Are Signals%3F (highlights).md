title:: What Are Signals? (highlights)
author:: [[tldraw.dev]]
full-title:: "What Are Signals?"
category:: #articles
url:: https://signia.tldraw.dev/docs/what-are-signals

- Highlights first synced by [[Readwise]] [[Mar 6th, 2023]]
	- **A signal** is a value that changes over time and whose change events can trigger side effects.
	  
	  **A signals library**, or framework, provides a cohesive set of tools for managing these changing values and their side effects in an automated way that ensures consistency. This allows developers to spend less time thinking about how updates are propagated through a system and more time focusing on what those updates should be. It also prevents whole classes of easy-to-introduce-but-hard-to-find bugs that can occur due to accidental mismanagement of derived state or side effects. ([View Highlight](https://read.readwise.io/read/01gtqd137mcvezejwaay0w2rk3))
	- Root values
	  
	  A root value is any state value that is updated directly, normally in response to external events, e.g. user input. ([View Highlight](https://read.readwise.io/read/01gtqd1s1ex5c31tzzzw476kjb))
	- Derived values
	  
	  A derived value is any state value that is computed exclusively by looking at other state values. ([View Highlight](https://read.readwise.io/read/01gtqd1nddbrpfhxym8h173jyg))
	- Side effects
	  
	  A side effect is any process which runs in response to a state change event. ([View Highlight](https://read.readwise.io/read/01gtqd1jndty3p86fjt3pqvqhc))
	- ![Push signals](https://signia.tldraw.dev/img/what-are-signals-push-light.png) ([View Highlight](https://read.readwise.io/read/01gtqd3t4mjwsdrqscnq296atx))
		- **Note**: When you change a root value, any derived values that read from it are immediately updated, and so on, from left to right.
	- ![Push signals](https://signia.tldraw.dev/img/what-are-signals-pull-light.png) ([View Highlight](https://read.readwise.io/read/01gtqd3w4gjffe3avqmw3pcpsf))
		- **Note**: When you change a root value, any side effects that might need to execute are notified. Upstream derived values are only recomputed if they are read from.