title:: The New Client Extension... (highlights)
author:: [[@ryanchenkie on Twitter]]
full-title:: "The New Client Extension..."
category:: #tweets
url:: https://twitter.com/ryanchenkie/status/1600516916191240192

- Highlights first synced by [[Readwise]] [[Dec 8th, 2022]]
	- The new Client Extensions feature in @prisma 4.7 opens up some great possibilities for enforcing data access restrictions.
	  
	  A common pattern:
	  
	  * admin users need to see all data
	  * external users only get to see their own data
	  
	  Let's look at how to handle this with `$extends` 👇 
	  
	  ![](https://pbs.twimg.com/media/FjYtptaVUAAxsQ3.jpg) ([View Tweet](https://twitter.com/ryanchenkie/status/1600516916191240192))
		- **Note**: Thread
	- These kinds of data lookup restrictions at the app level are often enforced in each and every query by taking a value from the user's session and scoping the query to it. 
	  
	  ![](https://pbs.twimg.com/media/FjYtqCzVUAE0VPy.jpg) ([View Tweet](https://twitter.com/ryanchenkie/status/1600516922927329282))
	- The problem is that when the app starts to grow and more developers are working on it, it can become easy to forget to scope down queries in this way.
	  
	  Imagine a query that surfaces sensitive info for all users and each user of the app gets to see it. Bad news. ([View Tweet](https://twitter.com/ryanchenkie/status/1600516925729054720))
	- To better protect against this, we can use the `query` level of Prisma Client Extensions to scope down the query in each and every place it is called.
	  
	  Let's say we have the following query. 
	  
	  ![](https://pbs.twimg.com/media/FjYtqkwVUAIIrxK.jpg) ([View Tweet](https://twitter.com/ryanchenkie/status/1600516931840143361))
	- It does just what it should and returns all the invoices in the table.
	  
	  In this case, just two records.
	  
	  Note that there's a different customer for each of the records. 
	  
	  ![](https://pbs.twimg.com/media/FjYtq9LVQAArj70.jpg) ([View Tweet](https://twitter.com/ryanchenkie/status/1600516938811133952))
	- As is, this query is the kind that could lead to data leaks if it's used in the wrong spot.
	  
	  But what if we could get a special Prisma Client instance that knows how to limit the query each time it's called?
	  
	  With the `query` level of Client Extensions, we can do just that. ([View Tweet](https://twitter.com/ryanchenkie/status/1600516941709393920))
	- Let's get ourselves a new instance that we'll call `nonAdminPrisma`.
	  
	  This instance should use `$extends` and should specify that whenever the `findMany` query on the `invoice` model is called, it should always ask to match by a `customerId`. 
	  
	  ![](https://pbs.twimg.com/media/FjYtrgXUoAA5VLH.jpg) ([View Tweet](https://twitter.com/ryanchenkie/status/1600516948290285568))
	- If we were to now use this Prisma Client instance instead, we'd get a result that is scoped to that customer. 
	  
	  ![](https://pbs.twimg.com/media/FjYtr7CVsAA8Dld.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FjYtsHgUYAAMRLV.jpg) ([View Tweet](https://twitter.com/ryanchenkie/status/1600516958008406016))
	- The value for `customerId` should come from the user's session. That way, no one can fake who they are from the front end.
	  
	  The way in which you'd get that value from a session and use it in your extended instance will differ depending on your specific setup. ([View Tweet](https://twitter.com/ryanchenkie/status/1600516960751472641))
	- What if we wanted to apply these rules to more than just that specific model?
	  
	  No problem. For that, we can use `$allModels`.
	  
	  This does assume, of course, that all the models are related to `Customer`. If that's not the case, we'd get a type error and would need to be specific. 
	  
	  ![](https://pbs.twimg.com/media/FjYtsnHUYAAZyeA.jpg) ([View Tweet](https://twitter.com/ryanchenkie/status/1600516967311368192))
	- Prisma Client Extensions is a great feature and I'm excited to see what can be done with it.
	  
	  I think it's the right level of abstraction for being both flexible and powerful at the same time 🎉 ([View Tweet](https://twitter.com/ryanchenkie/status/1600516970218016773))
	- If you're new to Prisma and would like to get up-to-speed quickly, check out my free getting started course here: https://t.co/pAoTLzwJ8P ([View Tweet](https://twitter.com/ryanchenkie/status/1600516972722077696))