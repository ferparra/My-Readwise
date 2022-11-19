title:: Introducing Domain-Oriented Microservice Architecture (highlights)
author:: [[eng.uber.com]]
full-title:: "Introducing Domain-Oriented Microservice Architecture"
category:: #articles
url:: https://eng.uber.com/microservice-architecture/

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- Understanding dependencies between services can become quite difficult, as calls between services can go many layers deep. A latency spike in the nth dependency can cause a cascade of issues upstream. Visibility into what’s actually happening is impossible without the right tools, making debugging difficult.
	- Instead of orienting around single microservices, we oriented around collections of related microservices. We call these domains.
	  We further create collections of domains which we call layers. The layer that the domain belongs to establishes what dependencies the microservices within that domain are allowed to take on. We call this layer design.
	  We provide clean interfaces for domains that we treat as a single point of entry into the collection. We call these gateways.
	  Finally, we establish that each domain should be agnostic to other domains, which is to say, a domain shouldn’t have logic related to another domain hard coded inside of its code base or data models. Since frequently teams do need to include logic in another team’s domain (for example, custom validation logic or some meta context on a data model), we provide an extension architecture to support well defined extension points within the domain.
	- think carefully about the logical role of each collection.
	- our map search services constitute a domain, fare services are a domain, matching platform (matching riders and drivers) are a domain
	- tend to think of gateways exclusively as a single entry-point into a collection of underlying services, which we call a domain