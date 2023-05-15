title:: Problem: You Want to Res... (highlights)
author:: [[@housecor on Twitter]]
full-title:: "Problem: You Want to Res..."
category:: #tweets
url:: https://twitter.com/housecor/status/1652641989773410306

- Highlights first synced by [[Readwise]] [[May 1st, 2023]]
	- Problem: You want to reset React state when a component’s props change.
	  
	  Solution: Change the component’s key when the props change. 
	  
	  When the key changes, React deletes the old component. It creates a new instance that uses the default state.
	  
	  No useEffect required. 😎 
	  
	  ![](https://pbs.twimg.com/media/Fu9c1yOXsAAn4xQ.jpg) ([View Tweet](https://twitter.com/housecor/status/1652641989773410306))
		- **Note**: Thread
	- Two more points:
	  
	  1. Why not use useEffect? Because resetting state via useEffect is error prone. As new state is added, someone may forget to update the useEffect call.
	  
	  2. Warning: If the component tree is expensive to render, consider resetting state via useEffect instead. ([View Tweet](https://twitter.com/housecor/status/1652695129289785345))
	- @gimenete And it’s a tradeoff, so agree can be a tough call: ([View Tweet](https://twitter.com/housecor/status/1652724623077699586))
	- Problem: "I don't like setting the key in the parent. It's not discoverable, has to be implemented in each usage, and breaks "encapsulation".  
	  
	  Solution: Wrap the component so it manages its own key. Do this in the component's file, and only export the wrapper.  Problem solved. 
	  
	  ![](https://pbs.twimg.com/media/Fu_FzgIXgAk1MP9.jpg) ([View Tweet](https://twitter.com/housecor/status/1652757164534972418))