title:: Tweets From Alex Nedelcu (highlights)
author:: [[@alexelcu on Twitter]]
full-title:: "Tweets From Alex Nedelcu"
category:: #tweets
url:: https://twitter.com/alexelcu

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- In case you don't have types fully expressing requirements, and thus need partial functions, where do you raise the exception for IO-driven or Future-driven functions?
	  
	  Immediately (since it's a bug) or in the context of IO or Future? 
	  
	  ![](https://pbs.twimg.com/media/FVwlptHXEAE5-zS.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FVwmICkXoAA1bt_.jpg) ([View Tweet](https://twitter.com/alexelcu/status/1539147165330710528))
	- In #Scala, how do you model maps with heterogeneous value types? Do you just use Any?
	  
	  I'd like a common-sense approach to make it safer. However, trying to apply reification (implicit values that reflect the type) will fail due to type inference + subtyping. 
	  
	  ![](https://pbs.twimg.com/media/FV_5OGPWYAEYt9g.jpg) ([View Tweet](https://twitter.com/alexelcu/status/1540223690306211840))