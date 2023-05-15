title:: I Spent the Weekend Upgr... (highlights)
author:: [[@steventey on Twitter]]
full-title:: "I Spent the Weekend Upgr..."
category:: #tweets
url:: https://twitter.com/steventey/status/1655951031665328130

- Highlights first synced by [[Readwise]] [[May 15th, 2023]]
	- I spent the weekend upgrading https://t.co/BGR54GWtHi to @nextjs App Router.
	  
	  Featuring:
	  ◆ Segment-level caching
	  ◆ Server components
	  ◆ Parallel & intercepting routes
	  ◆ Dynamic OG images + Metadata API
	  
	  Here's what I learned 🧵 https://t.co/6yNwGXgY8H ([View Tweet](https://twitter.com/steventey/status/1655951031665328130))
		- **Note**: Thread
	- 1. You can now cache individual fetch calls via segment-level caching.
	  
	  Combine static, dynamic, and revalidated data inside reusable components. E.g. on @dubdotsh's homepage:
	  ◆ GitHub star count: 60s
	  ◆ Tweet testimonials: 1hr
	  
	  The best part? Detailed logs for each cache hit 😍 
	  
	  ![](https://pbs.twimg.com/media/Fvsesg7acAEfP0J.jpg) ([View Tweet](https://twitter.com/steventey/status/1655951044860596230))
	- 2. Server components help you write less code.
	  
	  No more bulk fetching data inside getStaticProps and prop drilling all the way down to your child component – just use a server components instead.
	  
	  Here's the (much cleaner) index page after the migration: 
	  
	  ![](https://pbs.twimg.com/media/FvsetCLagAAMCDs.png) ([View Tweet](https://twitter.com/steventey/status/1655951052943032325))
	- 3. Parallel & intercepting routes are magical.
	  
	  You can now easily create @Instagram/@ProductHunt-esque modals that preview a page + change the route at the same time.
	  
	  On refresh, the page will default to the actual page.
	  
	  Docs → https://t.co/5kwcYsKNJJ https://t.co/YrYHn1o87C ([View Tweet](https://twitter.com/steventey/status/1655951123336036361))
	- 4. You can now easily generate dynamic social images.
	  
	  This is now built into @nextjs via the `ImageResponse` API. Write React + CSS/@tailwindcss, and Next.js automatically renders an Open Graph image for you.
	  
	  Docs → https://t.co/wXsscLtQzB
	  Demo ↓ https://t.co/fkkL28lvJk ([View Tweet](https://twitter.com/steventey/status/1655951127689719811))
	- As always, all the code for @dubdotsh is fully open-source → https://t.co/0I4VQC5tgT
	  
	  The code will continue to evolve in the next couple of weeks as I migrate the rest of the app itself over to the App Router, but feel free to refer to it! ([View Tweet](https://twitter.com/steventey/status/1655951131351343110))
	- @MoFromYYZ @nextjs @tailwindcss @shadcn Tailwind + @Radix_ui* ([View Tweet](https://twitter.com/steventey/status/1656030227099951104))