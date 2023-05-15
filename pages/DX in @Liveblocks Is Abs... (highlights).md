title:: DX in @Liveblocks Is Abs... (highlights)
author:: [[@ctnicholasdev on Twitter]]
full-title:: "DX in @Liveblocks Is Abs..."
category:: #tweets
url:: https://twitter.com/ctnicholasdev/status/1650849841139052551

- Highlights first synced by [[Readwise]] [[Apr 27th, 2023]]
	- DX in @liveblocks is absolutely mad.
	  
	  See this React hook?
	  
	  It grabs a real-time object named `person`. Every time the object changes, this hook automatically updates with the new value.
	  
	  No back end, no setting up WebSockets 🤯 it just works. 
	  
	  ![](https://pbs.twimg.com/media/Fuj_LgEaQAALylS.jpg) ([View Tweet](https://twitter.com/ctnicholasdev/status/1650849841139052551))
		- **Note**: Thread
	- What about updating the value? Well that's easy too.
	  
	  This function works like `useCallback`, but gives you access to real-time storage.
	  
	  Just call `changeName()` and `person` updates for every user. 
	  
	  ![](https://pbs.twimg.com/media/Fuj_L5MaAAYeIQu.jpg) ([View Tweet](https://twitter.com/ctnicholasdev/status/1650849849376636928))
	- Want to have a shared text input? Simple, just combine the two code snippets above, and you've got it.
	  
	  Multiple users, one input. https://t.co/OSYE74AVjR ([View Tweet](https://twitter.com/ctnicholasdev/status/1650849860114067456))
	- Here's what the full code looks like.
	  
	  It's even more impressive than you think though. When you start building more complex apps, a number of problems arise.
	  
	  ✦ Multiple users editing at once?
	  ✦ Nesting data structures?
	  ✦ Flaky connections?
	  ✦ Undo/redo for each user? 
	  
	  ![](https://pbs.twimg.com/media/Fuj_M_QaQAAv7fj.jpg) ([View Tweet](https://twitter.com/ctnicholasdev/status/1650849871505809409))
	- Conflict-free data types automatically handle all this for you, and even more. Not to mention, you can also read your real-time data with our:
	  
	  ✦ APIs
	  ✦ Webhooks
	  ✦ JavaScript package
	  ✦ DevTools extension
	  
	  https://t.co/wIQUqJFQlw ([View Tweet](https://twitter.com/ctnicholasdev/status/1650849874571849729))
	- The team actually wrote a fantastic interactive article on the problems of multiplayer undo/redo, really interesting stuff.
	  
	  → https://t.co/8VP87doEM5 https://t.co/3muVyHceXU ([View Tweet](https://twitter.com/ctnicholasdev/status/1650849896990375939))
	- I've only mentioned conflict-free data in this thread, but @liveblocks actually enables much more, for example:
	  
	  ✦ Displaying real-time presence
	  ✦ Broadcasting custom events
	  ✦ Document browsing
	  ✦ Customisable collaborative comments (coming soon)
	  + more! ([View Tweet](https://twitter.com/ctnicholasdev/status/1650849901692211200))
	- Building real-time collaborative apps like Figma or Notion was not an easy task—until @liveblocks came along. ([View Tweet](https://twitter.com/ctnicholasdev/status/1650849904431087616))