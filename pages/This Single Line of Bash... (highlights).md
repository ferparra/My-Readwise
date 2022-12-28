title:: This Single Line of Bash... (highlights)
author:: [[@TivadarDanka on Twitter]]
full-title:: "This Single Line of Bash..."
category:: #tweets
url:: https://twitter.com/TivadarDanka/status/1605888132200558592

- Highlights first synced by [[Readwise]] [[Dec 23rd, 2022]]
	- This single line of bash code will crash your system:
	  
	  :(){ : | : &};:
	  
	  It is a so-called fork bomb, duplicating itself with each call, eventually draining system resources dry.
	  
	  Here is how it works, character by character. ([View Tweet](https://twitter.com/TivadarDanka/status/1605888132200558592))
		- **Note**: Thread
	- In bash, functions are defined with the syntax
	  
	  foo() {
	- Thus, we have
	  
	  :() {
	    : | : &
	  }
	  
	  What is happening inside the function? There are two symbols here that need explaining: `|` and `&`. ([View Tweet](https://twitter.com/TivadarDanka/status/1605888137284067328))
	- `|` is called the pipe symbol, enabling us to pass a function's output into another function's input.
	  
	  For instance, `ls - l` outputs the contents of the current directory, line by line.
	  
	  On the other hand, `grep xy` returns the lines from a text where "xy" is found. ([View Tweet](https://twitter.com/TivadarDanka/status/1605888139737780224))
	- Thus,
	  
	  ls -l | grep xy
	  
	  yields all lines from `ls -l` for which "xy" is a substring. This is called piping. ([View Tweet](https://twitter.com/TivadarDanka/status/1605888142220742661))
	- What about the ampersand symbol `&`? The command
	  
	  foo &
	  
	  launches the function `foo` as a background job, returning the control to the caller.
	  
	  Let's put all of this together! ([View Tweet](https://twitter.com/TivadarDanka/status/1605888144607301632))
	- The function
	  
	  :() {
	    : | : &
	  }
	  
	  first calls itself, then pipes the result into itself as a background process. Thus, the process keeps on forking itself, hence the name fork bomb.
	  
	  As a result of this exponential growth, the system quickly runs out of its resources. ([View Tweet](https://twitter.com/TivadarDanka/status/1605888147136532480))
	- Overall, with a bit more user-friendly notation, this is the fork bomb:
	  
	  fork() {
	    fork | fork &
	  }
	  fork
	  
	  You might want to save all progress before trying this at home. ([View Tweet](https://twitter.com/TivadarDanka/status/1605888149787394050))
	- I usually talk about math here, but I am a curious person with lots of interests.
	  
	  If you have enjoyed this little thread, share it with your friends and give me a follow! I regularly post deep-dive explainers such as this. https://t.co/U7A5QPcuuM ([View Tweet](https://twitter.com/TivadarDanka/status/1605888152459042816))