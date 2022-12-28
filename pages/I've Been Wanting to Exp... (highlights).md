title:: I've Been Wanting to Exp... (highlights)
author:: [[@pdrmnvd on Twitter]]
full-title:: "I've Been Wanting to Exp..."
category:: #tweets
url:: https://twitter.com/pdrmnvd/status/1605620847741325312

- Highlights first synced by [[Readwise]] [[Dec 22nd, 2022]]
	- I've been wanting to explore streaming for a while, having lived most of my life as batchelor. A great way to get started is with CDC (Change Data Capture). At its core, CDC tracks what changed in your database and processes these as events. ([View Tweet](https://twitter.com/pdrmnvd/status/1605620847741325312))
		- **Note**: Thread
	- Every insert, change, and delete can be thought of as an event that happens to your underlying data. While there are many use-cases, the most common one is capturing changes in a transactional database and writing them to a data warehouse. ([View Tweet](https://twitter.com/pdrmnvd/status/1605620849037389824))
	- I got a sweet preview of the @striimteam upcoming release that makes it easy to ingest CDC streams from Postgres into BigQuery and Snowflake. Not having a real job though, I needed to create a some fake event data using the excellent fake_web_events package ([View Tweet](https://twitter.com/pdrmnvd/status/1605620850291400704))
	- You can find the code for that here: https://t.co/wxztIHvUHR. This writes a batch of events for real-time processing into a Postgres instance. ([View Tweet](https://twitter.com/pdrmnvd/status/1605620851839094785))
	- From there I then connect the PostgreSQL reader to an Output Stream that feeds into BigQuery for streaming writes. You can even do transformations along the way, e.g. if you want to make and aggregate data, or even add multiple outputs, if you want to write to S3. 
	  
	  ![](https://pbs.twimg.com/media/FkhPEsfUUAApGo_.jpg) ([View Tweet](https://twitter.com/pdrmnvd/status/1605620853181333504))
	- Once that's hooked up, I just run the python script and it starts sending events to Postgres which you can see pretty much immediately in BigQuery. Tada, you just created your first stream. Pretty slick! 
	  
	  ![](https://pbs.twimg.com/media/FkhPNnZVUAEr97C.jpg) ([View Tweet](https://twitter.com/pdrmnvd/status/1605620854842200065))