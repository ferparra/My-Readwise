title:: 1/ Update on the New Nex... (highlights)
author:: [[@nextjs on Twitter]]
full-title:: "1/ Update on the New Nex..."
category:: #tweets
url:: https://twitter.com/nextjs/status/1549841497822056454

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- 1/ Update on the new Next.js router, with support for nested layouts and React Server Components.
	  
	  This is the biggest update to Next.js since it was released and incorporates many features from React 18.
	  
	  We made a quick demo to show some of the features. https://t.co/riDXgtozcH ([View Tweet](https://twitter.com/nextjs/status/1549841497822056454))
		- **Note**: Thread
	- 2/ This new router stands on the shoulders of React 18:
	  
	  ◆ Pages and Layouts are Server Components by default, sending less code to the client
	  ◆ Interfaces are non-blocking and can be interrupted if higher priority work happens like transitions ([View Tweet](https://twitter.com/nextjs/status/1549841501781479425))
	- 3/ Layouts can be nested and shared across routes. On navigation, layouts do not re-render, meaning they preserve state and remain interactive.
	  
	  This enables developers to more easily build complex application layouts and more ergonomically handle success/error/loading states. ([View Tweet](https://twitter.com/nextjs/status/1549841503165550592))
	- 4/ Optimistic loading states using server routing.
	  
	  When loading UI is provided, navigation is instant and can be shown immediately while a request is made to the server. Otherwise, transitions will suspend with `startTransition`.
	  
	  Pages remain interactive during transitions. https://t.co/rh7qExkFXi ([View Tweet](https://twitter.com/nextjs/status/1549841537403691008))
	- 5/ On navigation, the “payload” for Server Components is stored in the client-side cache.
	  
	  ◆ Soft pushes don’t refetch from the server, making navigation instant
	  ◆ Hard pushes invalidate the “slice” of data from the server, allowing you to get fresh data ([View Tweet](https://twitter.com/nextjs/status/1549841541094686720))
	- 6/ We're actively working on implementing the new router.
	  
	  For more information, check out the original RFC. 
	  
	  https://t.co/j5o7WIeREZ ([View Tweet](https://twitter.com/nextjs/status/1549841542470328322))