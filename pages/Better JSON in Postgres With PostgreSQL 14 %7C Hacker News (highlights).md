title:: Better JSON in Postgres With PostgreSQL 14 | Hacker News (highlights)
author:: [[news.ycombinator.com]]
full-title:: "Better JSON in Postgres With PostgreSQL 14 | Hacker News"
category:: #articles
url:: https://news.ycombinator.com/item?id=27358977

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- MySQL can handle many more connections per instance than postgres. Often when you have a high-transaction database in prod with postgres, you need something like pgbouncer to handle connection pooling or you'll have a bad time.
	- Connection scaling in postgres works better with the more recent versions. Still, you might indeed want to implement a connection pool for your PG instance if you have large swathes of mostly idle connections due to the single-backend-per-connection constraint of postgresql.