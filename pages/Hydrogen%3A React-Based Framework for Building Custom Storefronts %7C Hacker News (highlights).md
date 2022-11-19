title:: Hydrogen: React-Based Framework for Building Custom Storefronts | Hacker News (highlights)
author:: [[news.ycombinator.com]]
full-title:: "Hydrogen: React-Based Framework for Building Custom Storefronts | Hacker News"
category:: #articles
url:: https://news.ycombinator.com/item?id=29150634

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- unlike SSR frameworks, it doesn't require downloading full bundles of JS and raw data to re-render and hydrate your entire UI client-side. This is also the direction Next.js is heading ([2] and [3]), and will have significant ramifications for both architecture and performance of React applications for years to come.
	- With React's new <Suspense>, the ugly SSR ergonomics disappear.  Suspense allows data to be awaited during rendering, instead of it needing to be preloaded out-of-band.This means that code for data loading can be contained completely within the relevant component, and not also duplicated within SSR preload functions.