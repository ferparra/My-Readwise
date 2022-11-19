title:: Gossip Dissemination (highlights)
author:: [[martinfowler.com]]
full-title:: "Gossip Dissemination"
category:: #articles
url:: https://martinfowler.com/articles/patterns-of-distributed-systems/gossip-dissemination.html

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- In a cluster of nodes, each node needs to pass metadata information it has, 
	   to all the other nodes in the cluster, without depending on a shared storage. 
	   In a large cluster, if all servers communicate with all the other servers, 
	   a lot of network bandwidth can be consumed. 
	   Information should reach all the nodes even when some network 
	   links are experiencing issues.