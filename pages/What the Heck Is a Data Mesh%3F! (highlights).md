title:: What the Heck Is a Data Mesh?! (highlights)
author:: [[cnr.sh]]
full-title:: "What the Heck Is a Data Mesh?!"
category:: #articles
url:: https://cnr.sh/essays/what-the-heck-data-mesh

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- It should surprise no one that a modern service stack is decentralized (a). Such stacks typically have hundreds or thousands of different services owned by dozens or hundreds of teams (a). Each team is left to define, build, and own its APIs.
	- But application developers don’t always have the skills necessary to define well-factored APIs or troubleshoot complex deployment issues. Federated governance (c) through service infrastructure teams, DevOps culture, and embedded site reliability engineers (SREs) acts as a counter-weight to decentralization.
	- Data pipelines aren’t new—it’s ETL—but the who is new. Centralized teams aren’t responsible for the transfer and transformation, application developers are. A decentralized data platform must be built. Automated pipeline generation tools can be built on top of Airflow, Prefect, and dbt. Application engineers can define their data products and transformations, and tools can auto-generate their transformation workflows.
	- Many service stacks begin with no clear set of standards. Teams build services using their own frameworks and tools, and don’t adhere to REST or gRPC best practices. What emerges is a distributed monolith with poorly documented APIs.