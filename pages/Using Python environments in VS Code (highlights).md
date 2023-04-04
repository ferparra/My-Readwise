title:: Using Python environments in VS Code (highlights)
author:: [[visualstudio.com]]
full-title:: "Using Python environments in VS Code"
category:: #articles
url:: https://code.visualstudio.com/docs/python/environments
tags:: #[[python]]

- Highlights first synced by [[Readwise]] [[Apr 2nd, 2023]]
	- There are two types of environments that you can create for your workspace: **virtual** and **conda** environments. ([View Highlight](https://read.readwise.io/read/01gwxsktqawt1y0hq8778nd08x))
	- A [**virtual environment**](https://docs.python.org/3/glossary.html#term-virtual-environment) is a built-in way to create an environment to isolate the packages you install per workspace. A virtual environment creates a folder that contains a copy (or symlink) to a specific interpreter. When you install packages into a virtual environment it will end up in this new folder so that they are not interspersed with other packages used or needed by other workspaces. ([View Highlight](https://read.readwise.io/read/01gwxskhdcafe0paskxdcx79ww))
	- Virtual environments related to the workspace but stored globally. For example, [Pipenv](https://pypi.org/project/pipenv/) or [Poetry](https://python-poetry.org/) environments that are located outside of the workspace folder. ([View Highlight](https://read.readwise.io/read/01gwxsm7yqexeb9q2bc5h70nhc))
	- [Select and activate an environment](https://code.visualstudio.com/docs/python/environments#_select-and-activate-an-environment)
	  
	  As [mentioned earlier](https://code.visualstudio.com/docs/python/environments#_where-the-extension-looks-for-environments), the Python extension tries to find and then select what it deems the best environment for the workspace. If you would prefer to select a specific environment, use the **Python: Select Interpreter** command from the **Command Palette** (⇧⌘P). ([View Highlight](https://read.readwise.io/read/01gwxsnfe1177eth6kd1haw9k3))