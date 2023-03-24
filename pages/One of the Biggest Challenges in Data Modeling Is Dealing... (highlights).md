title:: One of the Biggest Challenges in Data Modeling Is Dealing... (highlights)
author:: [[Ergest Xheblati]]
full-title:: "One of the Biggest Challenges in Data Modeling Is Dealing..."
category:: #articles
url:: https://twitter.com/ergestx/status/1630942753742888960
tags:: #[[data engineering ]]

- Highlights first synced by [[Readwise]] [[Mar 12th, 2023]]
	- In data warehousing terms this is known as slowly changing dimensions (SCDs) and there are several options, each with its own trade offs in complexity and ease of use.
	  
	  1. Store in a single field and update each time it changes. You have current state but you lose history.
	  
	  * * *
	  
	  2. Take a snapshot of the table each time it changes and store a history. This captures everything but makes querying harder.
	  
	  3. Take a daily snapshot of the table regardless of changes. This makes querying easier but if a day is lost, it messes up all your queries.
	  
	  * * *
	  
	  4. Store the previous and current value in a history table. This is what Salesforce does in their history tables. You have the full history but again querying is hard.
	  
	  5. Ideally you would store an immutable log of changes that ensures full history tracking and is easy to query. ([View Highlight](https://read.readwise.io/read/01gv9jwz4exr9adqjky27vx6hx))