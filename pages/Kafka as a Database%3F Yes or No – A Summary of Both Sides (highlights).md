title:: Kafka as a Database? Yes or No – A Summary of Both Sides (highlights)
author:: [[davidxiang.com]]
full-title:: "Kafka as a Database? Yes or No – A Summary of Both Sides"
category:: #articles
url:: https://davidxiang.com/2021/01/10/kafka-as-a-database/

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- In computer science, a stream is a sequence of data elements made available over time. A stream can be thought of as items on a conveyor belt being processed one at a time rather than in large batches.
	- the “database inside out” approach is not for everyone. @narayanarjun and @frasergeorgew are right — if you need to maintain constraints before events are written (e.g. not selling more items than you have in stock), it’s easier to use a DB and CDC.
	- Databases and the records inside them are designed to be mutable. It’s both a great convenience and a great risk. If a table accidentally gets deleted, you might find yourself scrambling to restore your database from a backup. This is particularly painful in production.
	- As a permanent log of events, data will always have its historical context and can easily be audited