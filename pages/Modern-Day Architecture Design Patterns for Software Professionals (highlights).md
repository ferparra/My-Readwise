title:: Modern-Day Architecture Design Patterns for Software Professionals (highlights)
author:: [[medium.com]]
full-title:: "Modern-Day Architecture Design Patterns for Software Professionals"
category:: #articles
url:: https://medium.com/better-programming/modern-day-architecture-design-patterns-for-software-professionals-9056ee1ed977

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- principle of segregating the read (query) and write/updates (command) operations in a data store
	- CQRS pattern suggests using different data models for the read and writes operations
	- a sequence of domain events is stored as a journal, and an aggregated view of the journal gives the current state of the application
	- Before every booking, an aggregated view shows the available rooms by looking at the events journals
	- Most cloud-service providers support messaging services like Google Pub/Sub, Azure Service Bus, AWS SQS, etc. These services, in combination with strong consistent data stores, can be used to implement this pattern
	- The Strangler design pattern advocates creating a facade on top of your legacy and a new application, providing an abstracted view to the consumers