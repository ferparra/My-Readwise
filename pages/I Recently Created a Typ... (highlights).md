title:: I Recently Created a Typ... (highlights)
author:: [[@benmvp on Twitter]]
full-title:: "I Recently Created a Typ..."
category:: #tweets
url:: https://twitter.com/benmvp/status/1473823066333454336

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- I recently created a TypeScript generic utility type that recursively converted `Date` types into Firestore `Timestamp` types
	  
	  The type was fun to come up w/ cuz I learned a lot but it's also a bit complex. Lemme break down all the TS features line by line...
	  
	  /thread 🧵👇🏾 
	  
	  ![](https://pbs.twimg.com/media/FHL5PdYUYAIaROT.png) ([View Tweet](https://twitter.com/benmvp/status/1473823066333454336))
		- **Note**: Thread
	- `ToFirestore<>` takes a single generic type param, `MaybeDate`. If it is a `Date` type, then the "true" branch of the type conditional returns a `Timestamp` type instead. This base case of the recursive type serves as the crux of the mapping of `Date` ➡️ `Timestamp` type
	  
	   🧵👇🏾 
	  
	  ![](https://pbs.twimg.com/media/FHL6eiiVIAEAxK3.png) ([View Tweet](https://twitter.com/benmvp/status/1473823070678773761))
	- The "false" branch of the outer conditional begins a nested one that converts `Date` ➡️ `Timestamp` types of an array type by recursively calling `ToFirestore<>` on the array item type
	  
	  (the `infer` keyword auto-creates a new generic type that's the array items type)
	  
	   🧵👇🏾 
	  
	  ![](https://pbs.twimg.com/media/FHL8xCkVkAAcvfx.png) ([View Tweet](https://twitter.com/benmvp/status/1473823074810093568))
	- If `MaybeDate` is not a `Date` or array, we check if it's an object type using yet another nested conditional. The "true" branch uses TS mapped types to keep the same key types but recursively call `ToFirestore<>` to convert `Date` ➡️ `Timestamp` value types
	  
	   🧵👇🏾 
	  
	  ![](https://pbs.twimg.com/media/FHMEvLKVUAIVJAH.png) 
	  
	  ![](https://pbs.twimg.com/media/FHMEvLLVUAE5wlu.png) ([View Tweet](https://twitter.com/benmvp/status/1473823079096672257))
	- Finally, if we don't have a `Date`, array, or object we simply return the type back as the termination condition of our recursive type
	  
	  So `ToFirestore<string[]>`
	  ➡️ `Array<ToFirestore<string>>`
	  ➡️ `Array<string>` (or `string[]`)
	  
	   🧵👇🏾 
	  
	  ![](https://pbs.twimg.com/media/FHMF9LQVUAEoJqi.png) ([View Tweet](https://twitter.com/benmvp/status/1473823082963894272))
	- Creating this TypeScript recursive generic type expression was pretty fun cuz I learned lots about creating custom TS utility types. I also had to refactor a lot to get it down to a single type
	  
	  My latest post explains more on how it works as well
	  
	   🧵👇🏾
	  
	  https://t.co/wpqwCfNSoH ([View Tweet](https://twitter.com/benmvp/status/1473823085316825091))
	- FYI - If you work on a React component library or create reusable ones w/in your app, you'll definitely wanna understand why/when you should use patterns like polymorphic, controlled or compound components
	  
	  This throwback post will help you out 😄
	  
	   🧵👇🏾
	  
	  https://t.co/9GJ8Il3kqt ([View Tweet](https://twitter.com/benmvp/status/1473823088017960960))
	- Hope you enjoyed this week's thread. If you're interested in staying connected w/ my content on JS/TS, React, DivOps, and other frontend technologies, feel free to subscribe to the BenMVP Newsletter!
	  
	  Keep learning my friends. 🤓
	  
	  https://t.co/oouc00rytl ([View Tweet](https://twitter.com/benmvp/status/1473823090714968065))