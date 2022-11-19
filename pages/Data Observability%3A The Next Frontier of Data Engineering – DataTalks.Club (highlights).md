title:: Data Observability: The Next Frontier of Data Engineering – DataTalks.Club (highlights)
author:: [[datatalks.club]]
full-title:: "Data Observability: The Next Frontier of Data Engineering – DataTalks.Club"
category:: #articles
url:: https://datatalks.club/podcast/s03e03-data-observability.html

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- for an organization that is moving from a monolith to a microservice architecture — something that almost every organization is doing. As a result of that, there has been the rise of devops — teams that help, have a constant pulse on the health of their systems and make sure that all the applications and infrastructure are up and running.
	- Observability is this holistic view that includes monitoring, tracking, triaging of incidents to prevent downtime of those systems.
	- Usually micro services are some sort of web services. Tools like DataDog, NewRelic or even open source tools like Prometheus and grafana — they are tailored to these kinds of applications, to web services, something that is always running. While in the data world, we often have something different, we more often have batch processes rather than something that is up and running all the time.
		- **Tags**: #[[mlops]] #[[favorite]]
	- Lineage is basically a map — an auto discovered or auto reconstructed map of all the dependencies, both upstream and downstream, of your data assets. Lineage helps us answer the question of “if I have a freshness problem in a given table, what downstream assets are impacted by that?”