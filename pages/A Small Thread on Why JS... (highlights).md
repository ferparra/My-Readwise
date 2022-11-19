title:: A Small Thread on Why JS... (highlights)
author:: [[@sarah_edo on Twitter]]
full-title:: "A Small Thread on Why JS..."
category:: #tweets
url:: https://twitter.com/sarah_edo/status/1366068234370256897

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- A small thread on why JS devs might find Go interesting (this thread is not for Go devs, it is intentionally 101) 🧵
	  
	  1. Short variable declaration: 
	  
	  ![](https://pbs.twimg.com/media/EvU_gWqUYBUyQIH.jpg) ([View Tweet](https://twitter.com/sarah_edo/status/1366068234370256897))
		- **Note**: Thread
	- 2. The time package is really nice. For instance, you can import “time” and then use it like so: 
	  
	  ![](https://pbs.twimg.com/media/EvVAeKGVEAMsYNV.jpg) ([View Tweet](https://twitter.com/sarah_edo/status/1366069044516855814))
	- 3. You can import and alias packages very quickly. for instance, to import that package of time, you could say 
	  
	  import “time”
	  
	  or to import multiple package and/or alias them: 
	  
	  ![](https://pbs.twimg.com/media/EvVAsWdVcAISIJj.jpg) ([View Tweet](https://twitter.com/sarah_edo/status/1366069272716353541))
	- 4. range. A very declarative for loop, range will take the range of what’s provided and iterate. It doesn’t have to be integers either, as long as you have more than two indexes, you’re good.
	  
	  Example: 
	  
	  ![](https://pbs.twimg.com/media/EvVDT8CVIAYvlcY.jpg) ([View Tweet](https://twitter.com/sarah_edo/status/1366072181625483264))
	- 5. Go has its own built-in documentation system. Once go is installed (you can install it here https://t.co/aMb3Rw3qfN) you can run “go doc” and then any keyword in the terminal, and it will return a ton of information! Think like MDN docs in the terminal.
	  
	  Try it:
	  go doc fmt 
	  
	  ![](https://pbs.twimg.com/media/EvVDkWHVEAA-hV3.jpg) ([View Tweet](https://twitter.com/sarah_edo/status/1366072474530582532))
	- 6a. type declarations, even in functions, are straightforward! 
	  
	  ![](https://pbs.twimg.com/media/EvVDzIUUUAMdnW2.jpg) ([View Tweet](https://twitter.com/sarah_edo/status/1366072696195321857))
	- 6b. But we can declare a few at a time if they’re the same type, like: x, y int
	  
	  Here we’re specifying the type of the parameter as well as the type of the return after the parenths: 
	  
	  ![](https://pbs.twimg.com/media/EvVD-l-U4AEE0md.jpg) ([View Tweet](https://twitter.com/sarah_edo/status/1366072870951026690))
	- No agenda here, I just think Go is fun to work with! Here are resources if you want to learn, too:
	  
	  Tour of Go: https://t.co/ibbKscQB16
	  Go playground: https://t.co/hQeKJYJ7Ah
	  Frontend Masters course: https://t.co/Cm2qleoLpI
	  Write an interpreter in Go: https://t.co/gncu4gO8bl ([View Tweet](https://twitter.com/sarah_edo/status/1366073082402664448))