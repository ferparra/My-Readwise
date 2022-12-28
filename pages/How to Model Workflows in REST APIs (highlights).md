title:: How to Model Workflows in REST APIs (highlights)
author:: [[Kenneth Lange]]
full-title:: "How to Model Workflows in REST APIs"
category:: #articles
url:: https://kennethlange.com/how-to-model-workflows-in-rest-apis/

- Highlights first synced by [[Readwise]] [[Dec 21st, 2022]]
	- The easiest way to model the blog workflow is just to store the workflow state as an attribute ([View Highlight](https://read.readwise.io/read/01gms0m1nv2raz7ns2d27r1k2j))
	- model each workflow transition as a subresource and let clients to use HTTP’s **POST** method on these subresources to perform the transition. ([View Highlight](https://read.readwise.io/read/01gms0p0d94abac4cz6y0drkrp))
	- **STYLE****USE WHEN:****1. State Attribute**When there are no restrictions on the transitions. You can go from any state to any state at any time. The states are basically nothing more than a list of values.**2. Transition Links**There are limits to which states you can go to depending on the current state.**3. Transition Subresource**The workflow is configurable by users, so states and transitions among them are not fixed, but can be changed at runtime. ([View Highlight](https://read.readwise.io/read/01gms0r7mpena39jab53035hng))