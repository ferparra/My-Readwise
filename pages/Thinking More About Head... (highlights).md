title:: Thinking More About Head... (highlights)
author:: [[@criccomini on Twitter]]
full-title:: "Thinking More About Head..."
category:: #tweets
url:: https://twitter.com/criccomini/status/1396874537677967362

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Thinking more about headless BI, reverse ETL, and the "analytics is a mess" post. These things seem connected to me. Businesses need three things:
	  
	  1⃣A process for defining metrics
	  2⃣A single source of truth for the metrics
	  3⃣A way to get metrics to all systems.
	  
	  🧵 1/6 ([View Tweet](https://twitter.com/criccomini/status/1396874537677967362))
		- **Note**: Thread
	- 1⃣A process for defining good metrics
	  
	  @bennstancil's post, "Analytics is a mess", describes the problem well:
	  
	  https://t.co/GLwzYPfENJ
	  
	  tl;dr Metrics are squishy; you need to pick the right ones.
	  
	  🧵 2/6 ([View Tweet](https://twitter.com/criccomini/status/1396874538705580033))
	- 2⃣A single source of truth for the metrics
	  
	  Once you've defined metrics, you need a canonical location to store them.
	  
	  @AirbnbEng's Minerva post documents this well:
	  
	  https://t.co/zZxWh484sS
	  
	  As does @basecasevc's Headless BI post:
	  
	  https://t.co/UeYFuaENeS
	  
	  🧵 3/6 ([View Tweet](https://twitter.com/criccomini/status/1396874539632533504))
	- The two sources of truth that I see are DWH and an OLAP system (@ApachePinot, @druidio).
	  
	  @getdbt + DWH lets you version control and track your metrics.
	  
	  The OLAP systems don't yet have a standard "headless" tool (a la DBT). Metrics are still created in dashboards.
	  
	  🧵 4/6 ([View Tweet](https://twitter.com/criccomini/status/1396874540630777858))
	- 3⃣A way to get metrics to all systems.
	  
	  This is the "Reverse ETL" part of the story, and to me the least interesting. You need to get data from your source of truth into downstream systems.
	  
	  @getcensus and @keboola do this (and also (2)).
	  
	  🧵 5/6 ([View Tweet](https://twitter.com/criccomini/status/1396874541498961925))
	- Again, DWH seems ahead of realtime OLAP systems for "reverse ETL". OLAP systems are treated as a sink rather than a source right now. An area for growth/improvement.
	  
	  🧵 6/6 ([View Tweet](https://twitter.com/criccomini/status/1396874542392365060))