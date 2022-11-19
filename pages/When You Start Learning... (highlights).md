title:: When You Start Learning... (highlights)
author:: [[@mpocock1 on Twitter]]
full-title:: "When You Start Learning..."
category:: #tweets
url:: https://twitter.com/mpocock1/status/1412783977732128773

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- When you start learning XState, it can feel like you want to use it for EVERYTHING. To a hammer, everything looks like a nail.
	  
	  Here's how to reuse your favourite @reactjs libs with XState: ([View Tweet](https://twitter.com/mpocock1/status/1412783965182832642))
		- **Note**: Thread
	- 1: Queries
	  
	  Use a useEffect to send events to your state machine with the resulting data. You can take that data, assign it into context, and use it from there.
	  
	  Works with React Query, Urql, @apollographql 
	  
	  ![](https://pbs.twimg.com/media/E5s07SsWEAIuhB8.jpg) ([View Tweet](https://twitter.com/mpocock1/status/1412783968114692102))
	- 2: Forms
	  
	  Don't reimplement Formik, just use it. Take the submit event, and process is in XState.
	  
	  Works with Formik, React Hook Form, Final Form - anything with an onSubmit. 
	  
	  ![](https://pbs.twimg.com/media/E5s14zJWEAQSmaH.jpg) ([View Tweet](https://twitter.com/mpocock1/status/1412783971801444356))
	- 3: Routing
	  
	  Use named actions in your state machine, and implement them by passing options into your component. This allows you to directly call the hooks you're used to using.
	  
	  Pictured here with React Router, but works equally well in Next.js. 
	  
	  ![](https://pbs.twimg.com/media/E5s2275XwAESOGe.jpg) ([View Tweet](https://twitter.com/mpocock1/status/1412783975857373188))
	- Some day, I'd like to release libs which treat these use cases with the care they deserve in XState.
	  
	  @xstate/form
	  @xstate/query
	  @xstate/router
	  
	  But for now, the solutions above work well. ([View Tweet](https://twitter.com/mpocock1/status/1412783977732128773))