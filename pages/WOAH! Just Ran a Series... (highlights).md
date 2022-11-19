title:: WOAH! Just Ran a Series... (highlights)
author:: [[@ctyau on Twitter]]
full-title:: "WOAH! Just Ran a Series..."
category:: #tweets
url:: https://twitter.com/ctyau/status/1525231458402574339

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- WOAH! Just ran a series of denormalizing join queries that took 4 hrs on a 16 Node ra3.16xlarge #Redshift cluster in a flock of Lambdas running @DuckDB in  < 5 mins! That's the diff between $832 and $12! 💰💵⏱#awslambda #awsredshift #optimized #AWS ([View Tweet](https://twitter.com/ctyau/status/1525231458402574339))
		- **Note**: Thread
	- The issue w/clustered systems like Redshift is that if you join many dimension tables to a single fact table, each join is handled 1 at a time with interim BCASTS. But if the dimensions fit on a 10GB Lambda, @duckdb can be used to quickly port Redshift SQL into a parallel worker. ([View Tweet](https://twitter.com/ctyau/status/1525501673036201984))
	- With 1000 Lambdas working in parallel, I was able to crunch through 3000+ parquet files (about 1TB) in under 5 minutes. This is over 3GB/sec! The reason @duckdb can do this so quickly compared to Redshift is that all the joins happen in memory without spilling to disk. ([View Tweet](https://twitter.com/ctyau/status/1525503275201601537))