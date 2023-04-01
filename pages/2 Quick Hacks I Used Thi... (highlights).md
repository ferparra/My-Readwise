title:: 2 Quick Hacks I Used Thi... (highlights)
author:: [[@teej_m on Twitter]]
full-title:: "2 Quick Hacks I Used Thi..."
category:: #tweets
url:: https://twitter.com/teej_m/status/1640448376021094402

- Highlights first synced by [[Readwise]] [[Mar 28th, 2023]]
	- 2 quick hacks I used this week writing Python in a notebook –
	  
	  1/ memoization
	  
	  I have an expensive function that uses the GPT API. With Python's built-in functools, I can cache the result using the functools.cache function decorator.
	  
	  1-liner optimization that mostly just works 
	  
	  ![](https://pbs.twimg.com/media/FsQExK6akAAXh-R.jpg) ([View Tweet](https://twitter.com/teej_m/status/1640448376021094402))
		- **Note**: Thread
	- 2/ Random sample button
	  
	  With the button component in @_hex_tech you can make a random sample button! Quickly pull out a few rows of your dataframe and apply a transformation to them.
	  
	  In this example I detect one-word edits to a news headline and transform it to HTML. https://t.co/eaPF73W3ra ([View Tweet](https://twitter.com/teej_m/status/1640448380202782720))
	- To make the button work, first check if the button was clicked, then take your Pandas dataframe and call df.sample(...)
	  
	  When the button hasn't been clicked yet, I use a fixed random seed (random_state=42) to ensure it's always the same data on the first run. 
	  
	  ![](https://pbs.twimg.com/media/FsQKaL1aQAAwNBh.png) ([View Tweet](https://twitter.com/teej_m/status/1640448383713435648))
	- @_hex_tech please write a better table viz component, the current one is unusable for text data ([View Tweet](https://twitter.com/teej_m/status/1640449068391608320))