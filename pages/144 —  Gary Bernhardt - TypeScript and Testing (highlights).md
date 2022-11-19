title:: 144 —  Gary Bernhardt - TypeScript and Testing (highlights)
author:: [[Full Stack Radio]]
full-title:: "144 —  Gary Bernhardt - TypeScript and Testing"
category:: #podcasts
url:: https://share.snipd.com/episode/cf64770a-7b74-4e9b-a699-08af98422c69

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Typescript
	  
	  Summary:
	  Typescript lets you write complex code without worrying about the wiring up of o ents. You can focus on very complex, tpe, fine grain tests for the corps logic of the system. The type overhead is quite small when programming, but the test overhead that is saved is massive. It requires no incremental work when i write new content or new components. Just kind of works for free.
	  
	  Transcript:
	  Speaker 2
	  Now that there are a few points that are actually tested, but they're kind of factored out, like a reducer kind of stuff, like the actuall reducer, not like s racket component testing, but just like there's some airy piece of logic that i'd extracted and wrote a test for because it was easier to write the code if i had tests while i was writing it, sort of thing.
	  
	  Speaker 1
	  Ye, exactly. A and that's not to say that the front end is never tested, because we have some cypress tests tat drive a browser. So our tests actually step through every single lesson in the system, just to make sure that, like, nothing blows up. But that's moreof just a giant smoke test an soand it requires no incremental work when i write new content or new components. Just kind of works for free. So by having typescript in place and not having to worry about all the wiring up of o ents, i can focus on very complex, tpe, fine grain tests for the corps logic of the system. And i can have this nice high level test that runs through and makes sure nothing is totally broken. But i don't have to write a whole lot of just really boring like this component when it gets this prop it renders, you know, with this class, or whatever. I don't do any of that stuff. And a, i think it's worked really well. Like i i have no regrets about about switching the typescript for that purpose, because the type overhead is quite small when programming, but the test overhead that is saved is massive. I mean, we're talking about, i wrote a blog post with numbers in it, but i think it was something like, the system would be two point five times as many lines of code if i had done a standard, what was it? Two to one test o code ratio.
	  
	  Speaker 2
	  Can you think of an, like, a concrete example of something that you would have written a test for if you weren't using typescript, that you didn't write a test for? Now, and is also never or guaranteed to never break. Yes.
	  
	  Speaker 1
	  So. Em, i mean, the api is a great example. So we have this it it's a single page ap so we don't even do s s r. So the front is always making api requests to the back end on every page load and every page transition. And a most of that api code is actually untested, so we have tons of back and handlers for the api n points. And what they usually look like is a request is coming in. It's statically typed. The type is known. We use a library called iot s to dynamically make sure that the pay load actually matches the expected type, so you can'tke pass in, you know, weird, unexpected stuff and confuse ou. And and then that a back anda p i handler is going to take that request apart. So let's say, i don't know, am, let's sayi just the use of registering, right? So there's like, any mal field and, well, we don't have passwords, but there's any male field, am, so we're gon to pull that out of the pay load and then pass it on to a data base model. It's going to create the actual record. But the code that that takes the incoming a pi request apart and passes it along to the deeper parts. Is just completely untested. Theres therear no tests around it. And the reason is that there is almost never a conditional in there. So as long as the structure of the data coming in is correct, which we know through a combination of static types and io t s dynamic validation, then a, there's, i mean, i'm sure something could go wrong, but almost nothing that could go wrong. And i believe it is true that we have never had a run time failure due to that code.
	  
	  Speaker 2
	  It's untested. ([Time 0:12:58](https://share.snipd.com/snip/7b2e33e9-57c2-401d-af72-8085a6109d4b))