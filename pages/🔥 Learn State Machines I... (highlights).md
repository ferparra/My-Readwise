title:: 🔥 Learn State Machines I... (highlights)
author:: [[@cassiozen on Twitter]]
full-title:: "🔥 Learn State Machines I..."
category:: #tweets
url:: https://twitter.com/cassiozen/status/1397624679137873920

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- 🔥 Learn State Machines in 10 tweets 👇 ([View Tweet](https://twitter.com/cassiozen/status/1397623475137699840))
		- **Note**: Thread
	- 1/10
	  
	  State Machines are often ignored in front-end but are extremely popular in other software development areas such as games and embedded systems.
	  
	  But there's a renewed interest for them, especially as our apps grow more complex. ([View Tweet](https://twitter.com/cassiozen/status/1397623539792965636))
	- 2/10
	  
	  What do they do? Imagine adding different possible "statuses" to your code (Like a video player, which can have status such as "playing" or "paused."). 
	  
	  A "State" in state machines is less like a "variable" and more like pre-defined "statuses" that your code might be in. ([View Tweet](https://twitter.com/cassiozen/status/1397623658714058754))
	- 3/10
	  
	  How does that help? You can make sure that certain things can only happen when your code is in a specific state. You cannot pause if it's "stopped". You cannot retry if it's still "loading." 
	  
	  You can also create rules for how and when your code can change its state/status. ([View Tweet](https://twitter.com/cassiozen/status/1397623732538019843))
	- 4/10
	  
	  But wait, you say. I can solve this with a simple boolean. isLoading. isPlaying. Done!
	  
	  I'll just leave this tweet from @shshaw for you: https://t.co/gkYFPNarNL ([View Tweet](https://twitter.com/cassiozen/status/1397623803492978689))
	- 5/10
	  
	  Let's do some data fetching with retry logic (Retry 3 times in case of error). I'll use the useStateMachine library but the format is similar to the more popular XState.
	  
	  Start by defining the possible states and the transitions (where can I go from a given state). 
	  
	  ![](https://pbs.twimg.com/media/E2VbkuaVUAIQViJ.jpg) ([View Tweet](https://twitter.com/cassiozen/status/1397623970497662979))
	- 6/10
	  
	  Some state machine libraries support "extended state", or "context". Since your regular "states" and finite and pre-determined, the context is where you store variable data, such as the fetched data and the retry count (we want to retry a maximum of 3 times) 
	  
	  ![](https://pbs.twimg.com/media/E2VbsEQUYAkqpau.jpg) ([View Tweet](https://twitter.com/cassiozen/status/1397624087313219584))
	- 7/10 
	  
	  State machines can run side effects when changing state. In our case, we try to fetch the data when entering the "loading" state. If it succeeds, we store the loaded data in the context and transition to the "loaded" state. If it fails, we transition to the "error" state. 
	  
	  ![](https://pbs.twimg.com/media/E2Vb0-5UcAEUD-F.jpg) ([View Tweet](https://twitter.com/cassiozen/status/1397624235904827393))
	- 8/10
	  
	  To Retry, we simply add an effect to the "error" state. Every time it enters "error", it will automatically increment the retry count and transition back to "loading" (which, in turn, will cause a re-fetch). 
	  
	  ![](https://pbs.twimg.com/media/E2Vb73gVkAESOdO.jpg) ([View Tweet](https://twitter.com/cassiozen/status/1397624355744456708))
	- 9/10
	  
	  Finally, to limit the number of times it can retry, we use a guard. Guards are functions that can allow or deny a transition. 
	  
	  ![](https://pbs.twimg.com/media/E2VcBO8VEAQLzGT.jpg) ([View Tweet](https://twitter.com/cassiozen/status/1397624460123906048))
	- 10/10
	  
	  State, context, transitions, effects & guards: These are all the major things you need to know to start using state machines. 
	  
	  For more info on useStateMachine (including this and other examples): https://t.co/XNpuKA3GCm
	  
	  For more info on XState: https://t.co/cgBLS6NqsV ([View Tweet](https://twitter.com/cassiozen/status/1397624679137873920))