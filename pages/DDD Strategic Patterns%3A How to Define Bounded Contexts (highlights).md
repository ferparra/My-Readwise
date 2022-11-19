title:: DDD Strategic Patterns: How to Define Bounded Contexts (highlights)
author:: [[codeburst.io]]
full-title:: "DDD Strategic Patterns: How to Define Bounded Contexts"
category:: #articles
url:: https://codeburst.io/ddd-strategic-patterns-how-to-define-bounded-contexts-2dc70927976e

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- Domain is the reality we inhabit: its entities, their behavior, laws they obey.
	- domain is called a Problem space
	- DDD implies domain decomposing into sub-domains, to ease their modelling and comprehension
	- contract of a service where the model is implemented. The contract can be represented as this service’s API or a set of events it publishes and consumes
	- It’s likely that we factor out an aggregate that sends http requests to external systems, with an intention to put it into a separate machine which can be scaled independently.
	- From the perspective of a domain expert, bounded context is an area where certain business-processes are implemented, the certain ubiquitous language is applied
	- some legacy-system that was built without DDD approach in mind
	- Cyrille Martraire stresses the importance of extracting bounded contexts based on their responsibilities and behavior. As a result, these contexts most probably would have different evolutionary forces and different motivation for change.
	- If DDD would explicitly claim that we should define our sub-domains by business-capabilities