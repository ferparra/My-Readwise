title:: We Wrote a Book About Building Business Applications in Go | Hacker News (highlights)
author:: [[news.ycombinator.com]]
full-title:: "We Wrote a Book About Building Business Applications in Go | Hacker News"
category:: #articles
url:: https://news.ycombinator.com/item?id=27140724

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- Inheritance is the number one cause of these turning into a massive shit show. It’s not a pattern that can ever be refactored into something else down the line once the decision is made. You end up with things that can’t be fixed and escalating costs like you have never seen just to keep the plates spinning.I always favour composition for that and very light weight service oriented architecture.Roughly the only thing that scales is things that have fairly strict command-query type segregation. Carefully designed REST interfaces are a good example of that.