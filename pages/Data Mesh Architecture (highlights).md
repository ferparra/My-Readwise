title:: Data Mesh Architecture (highlights)
author:: [[datamesh-architecture.com]]
full-title:: "Data Mesh Architecture"
category:: #articles
url:: https://www.datamesh-architecture.com/

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- A data product usually is a published data set that can be accessed by other domains, similar to an API.
	- To discover, access, and use the data product, it is described with metadata, including
	                            ownership and contact information, data location and access, update frequency,
	                            and a specification of the data model.
	- Policies on [[interoperability]] are the starting point.
	                            They allow other [[domain teams]] to use [[data]] products in a consistent way.
	- Global policies such as privacy and compliance are also common. Think about protection of personally identifiable information (PII) or industry-specific legal requirements.
	- Events are small, immutable, and highly domain oriented, such as OrderPurchased or ShipmentDelivered.
	                            Entities represent business objects such as shipments or articles with their state changing over time.
	- Domain events are a great fit to be ingested into the data platform as they represent relevant business facts.
	- For analytical use cases, it is often required to have both the latest state and the history of states over time.
		- **Tags**: #[[favorite]]
	- It shifts the responsibilities for data toward domain teams which are supported by a data platform team and a data enabling team.