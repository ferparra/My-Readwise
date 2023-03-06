title:: One of the Biggest Chall... (highlights)
author:: [[@ergestx on Twitter]]
full-title:: "One of the Biggest Chall..."
category:: #tweets
url:: https://twitter.com/ergestx/status/1630942753742888960

- Highlights first synced by [[Readwise]] [[Mar 6th, 2023]]
	- One of the biggest challenges in data modeling is dealing with data  mutability.
	  
	  Let's take a simple example:
	  
	  Order status is an attribute that changes over time. It can go from open to pending to confirmed to prepared, to shipped to delivered to returned to refunded. ([View Tweet](https://twitter.com/ergestx/status/1630942753742888960))
		- **Note**: Thread
	- On the application side, all you care about is current state so you can’t blame engineers from modeling it with a simple field called “status” and a field called “last_updated”
	  
	  But as an analyst you’d want to know the entire history of changes complete with exact timestamps. ([View Tweet](https://twitter.com/ergestx/status/1630942755311501313))
	- So how do you do it?
	  
	  CDC (change data capture) tools can be used to generate a stream of changes on a given table. Snowflake can also so this with their streaming tables.
	  
	  But then how do you store it in the data warehouse? ([View Tweet](https://twitter.com/ergestx/status/1630942757106614273))
	- In data warehousing terms this is known as slowly changing dimensions (SCDs) and there are several options, each with its own trade offs in complexity and ease of use.
	  
	  1. Store in a single field and update each time it changes. You have current state but you lose history. ([View Tweet](https://twitter.com/ergestx/status/1630942760059432963))
	- 2. Take a snapshot of the table each time it changes and store a history. This captures everything but makes querying harder.
	  
	  3. Take a daily snapshot of the table regardless of changes. This makes querying easier but if a day is lost, it messes up all your queries. ([View Tweet](https://twitter.com/ergestx/status/1630942761506553857))
	- 4. Store the previous and current value in a history table. This is what Salesforce does in their history tables. You have the full history but again querying is hard.
	  
	  5. Ideally you would store an immutable log of changes that ensures full history tracking and is easy to query. ([View Tweet](https://twitter.com/ergestx/status/1630942763175796738))
	- The ActivitySchema model is the only method that stores an immutable log of changes. Querying is still not easy but far better than the above methods. ([View Tweet](https://twitter.com/ergestx/status/1630942764950073345))