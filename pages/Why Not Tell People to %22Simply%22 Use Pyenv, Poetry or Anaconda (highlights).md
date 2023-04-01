title:: Why Not Tell People to "Simply" Use Pyenv, Poetry or Anaconda (highlights)
author:: [[Nobody has time for Python]]
full-title:: "Why Not Tell People to "Simply" Use Pyenv, Poetry or Anaconda"
category:: #articles
url:: https://bitecode.substack.com/p/why-not-tell-people-to-simply-use
tags:: #[[python]]

- Highlights first synced by [[Readwise]] [[Apr 1st, 2023]]
	- Using “-m” forces the users to know what Python they use. It’s too easy to install something for one Python and call it from another one. ([View Highlight](https://read.readwise.io/read/01gwxp9q99yt0728qejg3m7xqz))
	- Using a virtualenv removes most PATH, PYTHONPATH, permission and version issues, by design (but not all, hence -m even in venv). It will also prevent users for making more of a mess (like calling sudo). ([View Highlight](https://read.readwise.io/read/01gwxp9zzgqkwv5dd5qva3n5nm))
	- Using standard pip and venv means no chicken and eggs issue for installing the tools. Installing something outside of an env to manage an env is already setting up people for failure. So we use as few dependencies as possible. They work with “-m” and you will find tons of materials to help you when things go wrong. They are cross-platform. They will still be here tomorrow. ([View Highlight](https://read.readwise.io/read/01gwxpan2hkj5pcd10wrgrfb70))
	- The bottom line is: *provide a single procedure that will let most people do their job and have the highest possible rate of success.* ([View Highlight](https://read.readwise.io/read/01gwxpd4w8fk4t36cb1wrsdy6a))
	- Sure, it’s not a big deal to install the Python headers for pyenv to work, or making sure PYTHONPATH points to the root directory of your project. ([View Highlight](https://read.readwise.io/read/01gwxpdvtrnzn2bhckpdamdk8h))
	- Python is interpreted, with the added trick of having many compiled 3rd party modules containing Fortran, C, or even assembly. ([View Highlight](https://read.readwise.io/read/01gwxpfkszhqry0h08fym4zphj))