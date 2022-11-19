title:: Data-Oriented Architecture · My Reading List (highlights)
author:: [[blog.eyas.sh]]
full-title:: "Data-Oriented Architecture · My Reading List"
category:: #articles
url:: https://blog.eyas.sh/2020/03/data-oriented-architecture/

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Within a monolithic server, code could still be componentized and separated into
	  individual modules, but there’s no forced API boundary between the different
	  components of the program.
	- Service-oriented architectures (SOA), on the other hand, break up monolithic
	  programs into services for each independent, componentized function.
	- Rather than componentizing and federating data stores for each relevant
	  component, DOA mandates describing the data or state-layer in terms of a
	  centrally managed global schema.
	- Component-to-component interaction is minimized, instead favoring
	  interaction through the data layer