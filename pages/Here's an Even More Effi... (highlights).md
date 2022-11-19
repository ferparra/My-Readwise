title:: Here's an Even More Effi... (highlights)
author:: [[@steveruizok on Twitter]]
full-title:: "Here's an Even More Effi..."
category:: #tweets
url:: https://twitter.com/steveruizok/status/1488858696360861696

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Here's an even more efficient undo / redo manager in mobx. This time, instead of using snapshots / comparisons, we're using `deepObserve` and manually converting the changes it reports to JSON patches. https://t.co/CwlyCHPQ8T ([View Tweet](https://twitter.com/steveruizok/status/1488858696360861696))
		- **Note**: Thread
	- The big advantage here: we don't have to be constantly converting between the observable document and a regular JavaScript object. This gives makes the history much more efficient for performance and memory. ([View Tweet](https://twitter.com/steveruizok/status/1488858697979805698))
	- How it works: mobx-utils has a function called `deepObserve` that will call its listener whenever an observable changes. It passes along where the change occurred, what the operation was (add/remove/replace), and what the old/new values were.  https://t.co/pSOfCfOk72 ([View Tweet](https://twitter.com/steveruizok/status/1488858699389145089))
	- When the deepObserver lets us know about a change, we use its information to create "JSON patches" (https://t.co/EkKgsZs7D8) that describe how to undo and redo the change. Both patches are lists of operations like "at boxes/box1, change X to Y". 
	  
	  ![](https://pbs.twimg.com/media/FKl6gdUXMAs5VbV.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1488858701297594376))
	- The change format from `deepObserve` is different form the JSON patch format, however, so we need to that conversion by hand. Not too hard—credit to @jasonkohles for his work on https://t.co/Rpxv7AWtLG here. 
	  
	  ![](https://pbs.twimg.com/media/FKl6onfWQAE-D2P.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1488858703419875328))
	- We can then save these undo / redo patches in a stack and keep track of a pointer, just like we did before. https://t.co/utkzlYseae When we undo, we apply the current patch's undo or redo patch, depending on what whether we're undoing or doing. 
	  
	  ![](https://pbs.twimg.com/media/FKl7Q44WUAE4Jet.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1488858705575784451))
	- Making the undo/redo patches is very cheap. No snapshotting or comparisons required—all of that happens from within mobx/mobx-utils. ([View Tweet](https://twitter.com/steveruizok/status/1488858707693817863))
	- Here's a gist, too: https://t.co/VcgtD1AZlG ([View Tweet](https://twitter.com/steveruizok/status/1488858708989911044))