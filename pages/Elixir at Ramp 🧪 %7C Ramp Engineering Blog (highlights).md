title:: Elixir at Ramp 🧪 | Ramp Engineering Blog (highlights)
author:: [[engineering.ramp.com]]
full-title:: "Elixir at Ramp 🧪 | Ramp Engineering Blog"
category:: #articles
url:: https://engineering.ramp.com/elixir-at-ramp/

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Fantastic support for concurrency and parallelism that’s designed to avoid
	  system failure. See The soul of Erlang and Elixir by Saša Jurić. Ask
	  yourself as you watch “How would I implement a system with these properties in
	  Ruby, Node, Python, or Java?”
	- Correctness guarantees for partial failures and transient errors (see It’s
	  About Guarantees by Fred Hebert). Transient errors are extremely common
	  and most environments don’t have a great mechanism for handling them.
		- **Tags**: #[[favorite]]
	- Efficient string construction, especially useful in template rendering
	  (Elixir RAM and the Template of Doom by Evan Miller).
	- So as the Elixir app grows and grows, an entire class of uncertainty over “what
	  is this code in front of me doing” goes away, because there’s a ton of dangerous
	  behavior you know it’s not doing. You’re not home free! Function calls to
	  other modules could still call the network, or write to the DB, or delete files.
	  But you’re certain it’s not changing the variables you are looking at, and you
	  don’t need to keep a universe of state changes in your head to understand what
	  the code is doing.