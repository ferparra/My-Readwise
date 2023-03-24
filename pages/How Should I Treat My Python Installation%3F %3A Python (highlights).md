title:: How Should I Treat My Python Installation? : Python (highlights)
author:: [[reddit.com]]
full-title:: "How Should I Treat My Python Installation? : Python"
category:: #articles
url:: https://www.reddit.com/r/Python/comments/ys4dhe/how_should_i_treat_my_python_installation/

- Highlights first synced by [[Readwise]] [[Mar 14th, 2023]]
	- `python -m venv /path/to/new/virtual/environment`
	  
	  ..from you project level directory. Each project then has their own requirements installed in the venv folder without messing any other project or your system Python up. When you are working on that project just activate the venv and use pip install to put any packages into that folder. Most IDEs will have an option to auto enable that venv when you select the directory, or at least make it an easy 2/3 click process.
	  
	  Below is just a sample setup:
	  
	  `python -m venv .venv` ([View Highlight](https://read.readwise.io/read/01gvegyzg1ftgznvjs7qa0k4ee))
	- •   Add the .venv to your .gitignore
	    
	  •   Use `pip freeze > requirements.txt` to export a list of dependencies that can be uploaded so people can use the same file version you created the program with.
	    
	  •   To restore your venv folder or set it up on a different computer; clone the project from your git supplier, create the venv directory again, run `pip install -r requirements.txt` to download and install the dependencies you had on the original system. ([View Highlight](https://read.readwise.io/read/01gvegyt3p7trxmn050y5n2yw1))