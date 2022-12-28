title:: Thread Version of My @Re... (highlights)
author:: [[@pomber on Twitter]]
full-title:: "Thread Version of My @Re..."
category:: #tweets
url:: https://twitter.com/pomber/status/1576900746896736257

- Highlights first synced by [[Readwise]] [[Dec 23rd, 2022]]
	- Thread version of my @ReactAlicante talk: 
	  
	  ![](https://pbs.twimg.com/media/FeI-kBrX0AUjbi7.jpg) ([View Tweet](https://twitter.com/pomber/status/1576900746896736257))
		- **Note**: Thread
	- the title is a reference to @worrydream's talk https://t.co/L7YkpApLe9 
	  
	  ![](https://pbs.twimg.com/media/FeI_F-8XoAUlonY.png) ([View Tweet](https://twitter.com/pomber/status/1576900753561509888))
	- the first part of his talk shows how we are using computers to emulate old media
	  
	  using Photoshop to draw a fish emulates the drawing of a fish on a canvas instead of taking advantage of the computer to create a more accurate representation of a fish, one that moves and responds ([View Tweet](https://twitter.com/pomber/status/1576900756682129408))
	- I think the same happens with websites
	  
	  most (content) websites look like printed media, like books or magazines
	  
	  we are using the web as a magazine emulator ([View Tweet](https://twitter.com/pomber/status/1576900758905057280))
	- [to be continued...] ([View Tweet](https://twitter.com/pomber/status/1576900761103241216))
	- I wrote this blog post in 2017 when we were all blogging on Medium
	  
	  https://t.co/vlpu0YkrSe
	  
	  it's a typical tutorial where you build something step by step
	  
	  using the typical blog layout ([View Tweet](https://twitter.com/pomber/status/1576913354873982977))
	- I think that layout is a bad fit for the content
	  
	  1st, we have two things, code and explanations, going in parallel, but the layout forces you to put everything in sequence
	  
	  2nd, the code is something that changes over time, it's dynamic, and in this layout everything is static ([View Tweet](https://twitter.com/pomber/status/1576913357030199298))
	- after I published that post, for the next two years, those problems stayed in the back of my mind
	  
	  during that time I worked on two projects related to displaying code:
	- then in 2019 everyone was moving away from Medium
	  
	  so I followed the trend and made a new self-hosted blog re-using code from my previous projects 
	  https://t.co/VaaofXkhAw ([View Tweet](https://twitter.com/pomber/status/1576913361081540610))
	- the new version of the post (https://t.co/gGWVoYrCfj) makes it clear that we have 2 things in parallel, code and explanations
	  
	  code now changes in place, it's easier to follow
	  
	  it had much better reception than the original post, 3years later people still visit and share it a lot ([View Tweet](https://twitter.com/pomber/status/1576913363401338880))
	- [to be continued...] ([View Tweet](https://twitter.com/pomber/status/1576913365485568000))
	- if you write content for the web, and you want to make it more dynamic, you'll face two problems
	  
	  first, there aren't many UI patterns or guidelines to use as a reference
	  
	  second, there aren't many tools to help you write the content in that format ([View Tweet](https://twitter.com/pomber/status/1576939626836942849))
	- to be clear, I'm talking about content related to programming
	  
	  in other areas like data visualization, there are many well-established tools and patterns
	  
	  but we are seeing some improvement in programming content as well
	  
	  let's see some patterns that are starting to emerge ([View Tweet](https://twitter.com/pomber/status/1576939629852622848))
	- one pattern that is becoming popular in blog posts is to embed interactive widgets along the text
	  
	  the goal is to let the reader explore a concept at their own pace
	  
	  examples
	- a more extreme version of the interactive widget is the live editor
	  
	  here you give readers some code and let them edit it and see the result
	  
	  this gives the reader more freedom to explore but also less guidance from the author
	  
	  example https://t.co/fOmWawTvN7 https://t.co/Z3jmvovYct ([View Tweet](https://twitter.com/pomber/status/1576939676220334082))
	- another pattern is tabs
	  
	  it sounds basic and obvious, but it's not as widely used as you might think
	  
	  tabs follow a more general technique called details-on-demand, a piece of content you only show when the reader asks for it https://t.co/OB8LsG602j ([View Tweet](https://twitter.com/pomber/status/1576939705848893440))
	- you can also have something similar to tabs, but instead of changing the file you are showing, you focus on a different part of the code, or maybe even change the code
	  
	  I call this pattern the code spotlight
	  
	  examples
	- then we have the scrollytelling pattern
	  
	  here we use the scroll position to control what we show to the reader, usually code or demos
	  
	  examples
	- I've been talking about making things more dynamic, but some readers will need or prefer a static version of the content
	  
	  a good practice is to provide a way for the reader to fall back to a static version https://t.co/cJVzIsYMG2 ([View Tweet](https://twitter.com/pomber/status/1576939799264387073))
	- [to be continued...] ([View Tweet](https://twitter.com/pomber/status/1576939803324559360))
	- now let's see some tools
	  
	  use @mdx_js to import components in your markdown files
	  
	  this is ideal for embedding interactive widgets or live code editors
	- MDX also lets you pass markdown TO components
	  
	  this allows you to display the content in different ways without affecting the authoring experience
	  
	  it's a very powerful technique, I have an entire talk on this topic: https://t.co/RvgI5aehAY 
	  
	  ![](https://pbs.twimg.com/media/FePWdrYX0AIB8F-.png) ([View Tweet](https://twitter.com/pomber/status/1577354032686972933))
	- for embedding live code editors there are two great options
	- we also have a Spotlight component
	  
	  it works in a similar way, we pass a bunch of markdown and codeblocks inside the component and Code Hike will show them like this https://t.co/Uw55X668vp ([View Tweet](https://twitter.com/pomber/status/1577354072214183936))
	- another one is the Scrollycoding component
	  
	  the input is similar, and the output follows the scrollytelling pattern we saw before
	  
	  you can even provide a media query to display a static version of the same content https://t.co/P421QRsJYW ([View Tweet](https://twitter.com/pomber/status/1577354095366651904))
	- Code Hike has some default styling, but you can use CSS to customize it
	  
	  here for example I made a clone of Stripe docs, it is mostly MDX and CSS
	- recap
	  
	  the web is a powerful medium, but most technical content websites are not taking advantage of it
	  
	  we've seen some examples of websites that are going in the right direction, and we've seen some tools that can help you write this type of content ([View Tweet](https://twitter.com/pomber/status/1577354126006034433))
	- if you write technical content, remember that these tools & patterns exist (these and more)
	  
	  remember that you can provide a different reader experience without sacrificing authoring experience
	  
	  there's also a lot of space for innovation, you can help explore new patterns & tools ([View Tweet](https://twitter.com/pomber/status/1577354128216432641))
	- if you are interested in this topic, I'm starting a new place to hang out and share stuff
	  
	  it's still very new and under construction, but there's already a discord server and (maybe) a newsletter