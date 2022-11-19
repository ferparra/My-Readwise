title:: Working on a New Undo /... (highlights)
author:: [[@steveruizok on Twitter]]
full-title:: "Working on a New Undo /..."
category:: #tweets
url:: https://twitter.com/steveruizok/status/1487052071685734410

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Working on a new Undo / Redo manager that runs on mobx and JSON patches. Here's how it works! 🧵 
	  
	  ![](https://pbs.twimg.com/media/FKLlCQwXMAkhcrV.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1487052071685734410))
		- **Note**: Thread
	- First off, here's a CodeSandbox. Looks pretty simple but there's a lot going on. I've included my tests! https://t.co/ixiMjCSYTS ([View Tweet](https://twitter.com/steveruizok/status/1487052074307272705))
	- In our system, we're tracking changes to a "document". Each time the document changes, we generate a "snapshot" and compare it with our previous snapshot in order to create a "patch" that describes how to get from the current snapshot back to the previous. 
	  
	  ![](https://pbs.twimg.com/media/FKMAMe8WYAAL_HA.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1487052075771076609))
	- These patches are "JSON patches" (https://t.co/EkKgsZs7D8). Each patch is made up of a series of operations that will turn one object into another. In our case, our patches describe all of the operations needed to get from our current snapshot back to our previous snapshot. 
	  
	  ![](https://pbs.twimg.com/media/FKMC05SXEAoVd-V.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1487052077939499011))
	- We store these patches in a "stack". This is a list that has a "pointer" that refers to the current patch. We also keep around a snapshot from our last change (or the initial document, if we haven't changed anything yet). 
	  
	  ![](https://pbs.twimg.com/media/FKMFgJ4XEAkAj4H.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1487052082519683074))
	- 1️⃣ Let's say we make a change to our document. 
	  
	  ![](https://pbs.twimg.com/media/FKMKljkXIAIVV38.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1487052087431159813))
	- When our document changes, we first take a snapshot of the current document... 
	  
	  ![](https://pbs.twimg.com/media/FKMKqVvXwAMNnQv.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1487052092808302593))
	- ...and we compare it against our previous snapshot in order to create a new patch. Again, this patch describes all the steps needed to "undo" the new change. 
	  
	  ![](https://pbs.twimg.com/media/FKMK7fDWUAE90JK.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1487052097812107267))
	- Next, we push the new patch onto the stack and move the pointer up so that it points to our new patch. 
	  
	  ![](https://pbs.twimg.com/media/FKMLhW4XwAYbHD7.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1487052103331815424))
	- Finally, we save the snapshot we made of our current document as our new previous snapshot. (We can discard the old previous snapshot.) 
	  
	  ![](https://pbs.twimg.com/media/FKMLwtuXsAgfrw4.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1487052108692082691))
	- Now we're ready for the next change! 
	  
	  ![](https://pbs.twimg.com/media/FKMMQqGXMAUdiU4.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1487052113645613060))
	- 2️⃣ To undo a change, we apply the current patch (e.g. the one that the pointer is pointing to) to the current document. Applying a patch performs the patch's operations and will bring the state back to where it was before the most recent change. 
	  
	  ![](https://pbs.twimg.com/media/FKMMkvWWUAANLwx.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1487052118578114569))
	- Next, we take a snapshot of the new document... 
	  
	  ![](https://pbs.twimg.com/media/FKMMyHJXwAAipXG.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1487052123363856384))
	- And compare it with the previous snapshot in order to produce a new patch. This patch is our "redo", it lists the operations needed to go from our current document  (after undoing) back to what it was before we pressed "undo". 
	  
	  ![](https://pbs.twimg.com/media/FKMNBUQXMAQ1ENo.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1487052128824799234))
		- **Tags**: #[[favorite]]
	- We *replace* the current patch—the one we just applied—with this new "redo" patch, and move the pointer back to the previous patch. 
	  
	  ![](https://pbs.twimg.com/media/FKMOBHXWYAIxxir.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1487052134696767504))
	- And finally we set the current snapshot as our previous snapshot. 
	  
	  ![](https://pbs.twimg.com/media/FKMOREoXwA4loQ9.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1487052139650330625))
	- And again, we're ready for the next change! 
	  
	  ![](https://pbs.twimg.com/media/FKMOXVAX0AEGpOI.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1487052145039925251))
	- 3️⃣ If we pressed redo, then we would start by moving out pointer up. 
	  
	  ![](https://pbs.twimg.com/media/FKMO6aPXwAIP7Nj.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1487052150211555333))
	- We would then apply the current patch to the current document... 
	  
	  ![](https://pbs.twimg.com/media/FKMPJP8XEAElo9W.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1487052159069958146))
	- And then create a snapshot of the current document, compare it with the previous document to create a patch... 
	  
	  ![](https://pbs.twimg.com/media/FKMPh2MWQAEwkvS.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1487052164015001600))
	- And then *replace* the current patch with the new one. 
	  
	  ![](https://pbs.twimg.com/media/FKMPwoaWQAElf-F.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1487052168788160521))
	- Finally, we'd set the current snapshot as the previous snapshot... 
	  
	  ![](https://pbs.twimg.com/media/FKMQAPSXMAMhipk.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1487052173921951752))
	- And job done! 
	  
	  ![](https://pbs.twimg.com/media/FKMQHYFXIAULIxF.jpg) ([View Tweet](https://twitter.com/steveruizok/status/1487052178770599937))
	- But we're not done. The story continues! (in the next thread) ([View Tweet](https://twitter.com/steveruizok/status/1487052181014466564))