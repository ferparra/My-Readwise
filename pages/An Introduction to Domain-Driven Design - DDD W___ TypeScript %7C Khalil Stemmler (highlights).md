title:: An Introduction to Domain-Driven Design - DDD W/ TypeScript | Khalil Stemmler (highlights)
author:: [[khalilstemmler.com]]
full-title:: "An Introduction to Domain-Driven Design - DDD W/ TypeScript | Khalil Stemmler"
category:: #articles
url:: https://khalilstemmler.com/articles/domain-driven-design-intro/

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- Discover the domain model by interacting with domain experts and agreeing upon a common set of terms to refer to processes, actors and any other phenomenon that occurs in the domain.
		- **Tags**: #[[favorite]]
	- DDD's primary technical benefits are that it enables you to write expressive, rich and encapsulated software that are testable, scalable and maintainable
	- We use repositories in order to retrieve domain objects from persistence technologies. Using software design principles like the Liskov Subsitution Principle and a layered architecture, we can design this in a way so that we can easily make architecture decisions to switch between an in-memory repository for testing, a MySQL implementation for today, and a MongoDB based implementation 2 years from now.