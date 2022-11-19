title:: Bliki: CQRS (highlights)
author:: [[martinfowler.com]]
full-title:: "Bliki: CQRS"
category:: #articles
url:: https://martinfowler.com/bliki/CQRS.html

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- CQRS should only be used on specific portions of a
	  system (a BoundedContext in DDD lingo) and not the system as a whole. In this
	  way of thinking, each Bounded Context needs its own decisions on how
	  it should be modeled