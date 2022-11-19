title:: Using PostgreSQL as a Data Warehouse | Hacker News (highlights)
author:: [[news.ycombinator.com]]
full-title:: "Using PostgreSQL as a Data Warehouse | Hacker News"
category:: #articles
url:: https://news.ycombinator.com/item?id=27109960

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- Instead of updating tables build their replacements under a different name then rename them. This makes updating heavy-to-compute table instant. Works even for schemas: rebuild a schema  as schemaname_next rename the current to schemaname_old then rename schemaname_next to schemaname.
	- Keep all the source data raw and disable WAL, you don't need it for ETL.
	- Set memory limitis high.