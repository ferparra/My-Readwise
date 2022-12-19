title:: [@Tableau Tips] 💡  You... (highlights)
author:: [[@ladataviz on Twitter]]
full-title:: "[@Tableau Tips] 💡  You..."
category:: #tweets
url:: https://twitter.com/ladataviz/status/1587445035863351298

- Highlights first synced by [[Readwise]] [[Dec 7th, 2022]]
	- [@tableau tips] 💡 
	  
	  You can now create a date filter mixing predefined settings and custom dates and only show the start/end dates when "Custom" is selected 🥳
	  
	  That is possible with the latest version, 2022.3, and the  Dynamic zone visibility feature. 
	  
	  Let me show you how! https://t.co/rz9Ia63Mbj ([View Tweet](https://twitter.com/ladataviz/status/1587445035863351298))
		- **Note**: Thread
	- 1. Create three parameters:
	- 2. Create a date filter calculation.
	  
	  Depending on the user selection, it will filter the date in different ways.
	  
	  I chose the last 7 days, 30 days, and custom dates that the user can select with the start/end date parameter.
	  
	  Add that filter to the worksheets you want to filter. 
	  
	  ![](https://pbs.twimg.com/media/Fge4jL-XEAESWs0.jpg) ([View Tweet](https://twitter.com/ladataviz/status/1587445049092104195))
	- 3. Create a simple calculated field that will check if the period selector parameter is equal to the custom option. 
	  
	  (In my case, the custom option is 3).
	  
	  Name that field "Custom selected."
	  
	  This will return true (if "custom" is selected) or false otherwise. 
	  
	  ![](https://pbs.twimg.com/media/Fge5CfyWIAEFU4W.jpg) ([View Tweet](https://twitter.com/ladataviz/status/1587445053441642502))
	- 4. Assemble your dashboard:
	- 5. Add a visibility control:
	- 6. That's it! 
	  
	  This was a long-requested feature.
	  
	  It significantly improves your dashboard by only showing the users relevant information. 
	  
	  I hope you enjoy this mini Twitter tutorial! ([View Tweet](https://twitter.com/ladataviz/status/1587445126670032897))