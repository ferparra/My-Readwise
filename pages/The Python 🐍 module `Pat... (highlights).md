title:: The Python 🐍 module `Pat... (highlights)
author:: [[@mathsppblog on Twitter]]
full-title:: "The Python 🐍 module `Pat..."
category:: #tweets
url:: https://twitter.com/mathsppblog/status/1645458050726129665

- Highlights first synced by [[Readwise]] [[Apr 13th, 2023]]
	- The Python 🐍 module `pathlib` is amazing.
	  
	  Learning about it will make you 10x more productive*! 🚀
	  
	  If you want to work with files, you need to know about it!
	  
	  Let me show 5 of the most useful tools in this module 👇
	  
	  (*Actual numbers may vary. 🤡) 
	  
	  ![](https://pbs.twimg.com/media/FtXXXbCXwAIf7cy.jpg) ([View Tweet](https://twitter.com/mathsppblog/status/1645458050726129665))
		- **Note**: Thread
	- When using the module `pathlib`, most of the time you will want to use the class `Path`.
	  
	  That class will let you work with files, paths, and directories, in your operating system.
	  
	  So, let us get started! 
	  
	  ![](https://pbs.twimg.com/media/FtXXgBkWwAEjfrW.jpg) ([View Tweet](https://twitter.com/mathsppblog/status/1645458196901797888))
	- 📂 Check if a file/directory exists.
	  
	  If you need to figure out if a file or a directory exists, you create an instance of `Path` with the path you want to check and use the method `exists`: 
	  
	  ![](https://pbs.twimg.com/media/FtXXna0WwAEpbVY.jpg) ([View Tweet](https://twitter.com/mathsppblog/status/1645458332063264769))
	- 📂 Create a new directory.
	  
	  You can use the method `.mkdir` to create a directory.
	  
	  If the directory exists, you get an error.
	  
	  Unless you specify `exist_ok=True`.
	  Very helpful to make sure a folder exists before working inside it. 
	  
	  ![](https://pbs.twimg.com/media/FtXXw4wXsAUMBYz.jpg) ([View Tweet](https://twitter.com/mathsppblog/status/1645458491337760769))
	- 📂 Move/rename a file or directory.
	  
	  I always forget what this method is called but if you need to move/rename a file or a directory, you can use the method `.replace`.
	  
	  ❗Just be careful: if the target already exists, it will be REPLACED. 
	  
	  ![](https://pbs.twimg.com/media/FtXX4IlWYAIvr4Q.jpg) ([View Tweet](https://twitter.com/mathsppblog/status/1645458627162001408))
	- 📂 Find the parent of a file/directory.
	  
	  The property `.parent` can be used to retrieve the parent of a file/directory.
	  
	  In other words, use the property `.parent` go up the filesystem hierarchy.
	  
	  Also, `.parent` can obviously be “chained”: 
	  
	  ![](https://pbs.twimg.com/media/FtXYBg0XoAcZINo.jpg) ([View Tweet](https://twitter.com/mathsppblog/status/1645458786193223681))
	- 📂 Get the name of the file/directory.
	  
	  The property `.name` can be used to determine the name of a file or directory.
	  
	  For example, `.parent.⁣name` will retrieve the name of the directory a file is in. 
	  
	  ![](https://pbs.twimg.com/media/FtXYQxhXwAEa_8T.jpg) ([View Tweet](https://twitter.com/mathsppblog/status/1645459039365603332))
	- BONUS!
	  
	  📂✨ Find the folder a script is in.
	  
	  By using the class `Path`, the property `.parent`, and the dunder `__file__`, you can figure out the folder a Python script is in. 
	  
	  ![](https://pbs.twimg.com/media/FtXYZGwX0AADNSi.jpg) ([View Tweet](https://twitter.com/mathsppblog/status/1645459176653553671))
	- That's it for now!
	  
	  If you enjoyed this thread:
	  
	  👉 follow me @mathsppblog for more Python 🐍 knowledge; and
	  👉 retweet the tweet below to share this thread with your audience!
	  
	  What other tips do you have for `pathlib`?
	  Add them here 👇
	  
	  https://t.co/MXymnX3zQC ([View Tweet](https://twitter.com/mathsppblog/status/1645459346032144384))