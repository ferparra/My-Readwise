title:: Using Tactical DDD to Design Microservices - Azure Architecture Center (highlights)
author:: [[docs.microsoft.com]]
full-title:: "Using Tactical DDD to Design Microservices - Azure Architecture Center"
category:: #articles
url:: https://docs.microsoft.com/en-us/azure/architecture/microservices/model/tactical-ddd

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- The tactical patterns are applied within a single bounded context
	- Entities. An entity is an object with a unique identity that persists over time. For example, in a banking application, customers and accounts would be entities.
	- Value objects. A value object has no identity. It is defined only by the values of its attributes. Value objects are also immutable. To update a value object, you always create a new instance to replace the old one. Value objects can have methods that encapsulate domain logic, but those methods should have no side-effects on the object's state. Typical examples of value objects include colors, dates and times, and currency values.
		- **Tags**: #[[favorite]]
	- Aggregates. An aggregate defines a consistency boundary around one or more entities. Exactly one entity in an aggregate is the root. Lookup is done using the root entity's identifier. Any other entities in the aggregate are children of the root, and are referenced by following pointers from the root.
	- The purpose of an aggregate is to model transactional invariants. Things in the real world have complex webs of relationships. Customers create orders, orders contain products, products have suppliers, and so on. If the application modifies several related objects, how does it guarantee consistency? How do we keep track of invariants and enforce them?
		- **Tags**: #[[favorite]]
	- Traditional applications have often used database transactions to enforce consistency. In a distributed application, however, that's often not feasible. A single business transaction may span multiple data stores, or may be long running, or may involve third-party services. Ultimately it's up to the application, not the data layer, to enforce the invariants required for the domain. That's what aggregates are meant to model.
		- **Tags**: #[[software architecture]] #[[favorite]]