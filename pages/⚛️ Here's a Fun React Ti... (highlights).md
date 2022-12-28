title:: ⚛️ Here's a Fun React Ti... (highlights)
author:: [[@DavidKPiano on Twitter]]
full-title:: "⚛️ Here's a Fun React Ti..."
category:: #tweets
url:: https://twitter.com/DavidKPiano/status/1604870393084665856

- Highlights first synced by [[Readwise]] [[Dec 20th, 2022]]
	- ⚛️ Here's a fun React tip: `useReducer` is a better `useState`, and it's easier to adopt than you may think.
	  
	  Group related values together and spread them in the reducer. Then, updating is just:
	  
	  updateThing({ prop: newValue })
	  
	  And there's even more benefits to `useReducer`... 
	  
	  ![](https://pbs.twimg.com/media/FkWhrzHXkAA5tJS.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FkWhrzHXgAMy94c.jpg) ([View Tweet](https://twitter.com/DavidKPiano/status/1604870393084665856))
		- **Note**: Thread
	- When you centralize related data into a reducer, you can ensure data integrity no matter where the updates happen.
	  
	  This is harder to do with `useState` since you have to defensively program *everywhere* the setState calls are made; it's less reliable and easy to miss. 
	  
	  ![](https://pbs.twimg.com/media/FkWjcnSXwAIIm7J.jpg) ([View Tweet](https://twitter.com/DavidKPiano/status/1604870397564002305))
	- But the *real* reason to incrementally adopt `useReducer` is that refactoring to use explicit events becomes easier.
	  
	  Events are a great abstraction for understanding & organizing app logic better, especially as the logic gets more complex. 
	  
	  ![](https://pbs.twimg.com/media/FkWkHEYWYAAYWCg.jpg) ([View Tweet](https://twitter.com/DavidKPiano/status/1604870402798493696))
	- For the TypeScript lovers, I believe this is all you need:
	  
	  (data: Data, partialData: Partial<Data>): Data => {...} 
	  
	  ![](https://pbs.twimg.com/media/FkWm11gXgAI2BqL.jpg) ([View Tweet](https://twitter.com/DavidKPiano/status/1604872533282627585))
	- "fun" here means "controversial"; I know you all love your useStates. They're overused and lead to unsafe logic. ([View Tweet](https://twitter.com/DavidKPiano/status/1604873594852474885))
	- @MarcosNASAG @abooAyoob The "you can do this with a single useState too" arguments miss the point completely.
	  
	  It's as if I said "vegetables can taste good too, and there's more benefits..." and others saying "nah, candy tastes much better" – it's not just about the taste! ([View Tweet](https://twitter.com/DavidKPiano/status/1604906617530900480))