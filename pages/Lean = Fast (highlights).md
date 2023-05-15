title:: Lean = Fast (highlights)
author:: [[brandur.org]]
full-title:: "Lean = Fast"
category:: #articles
url:: https://brandur.org/fragments/lean-fast
tags:: #[[engineering management]]

- Highlights first synced by [[Readwise]] [[Apr 22nd, 2023]]
	- •   **Small teams *ship*.** Every IC in our org has a huge amount of personal discretion and is empowered to make decisions without sending up the chain for approval. We write code individually, communicate over Slack and GitHub in moderation, and pair when we need a higher-bandwidth channel to do something hard. ([View Highlight](https://read.readwise.io/read/01gygc3d9mx79ywq0ztr90sya5))
	- **There’s a right size of services.** We’re using a “macroservices” model with a frontend, API layer, and backend state machine, and unless something changes dramatically, those are all the services we ever plan to run. The frontend talks to the API by way of strongly-typed TypeScript bindings, making integration faster and more accurate, and we’ve optimized our development flows such that every frontend pull request spins up a review app that’s fully functional against a staging API, and is a single click to log into. Everything can be boostrapped to run locally in less than a minute by following quickstart instructions in READMEs. ([View Highlight](https://read.readwise.io/read/01gygc4qjx82ygf4qzq4txagsz))