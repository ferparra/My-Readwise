title:: Testing React Components With Jest and Enzyme (highlights)
author:: [[Artem Sapegin]]
full-title:: "Testing React Components With Jest and Enzyme"
category:: #articles
url:: https://medium.com/p/41d592c174f

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- Shallow rendering renders only component itself without its children. So if you change something in a child component it won’t change shallow output of your component. Or a bug, introduced to a child component, won’t break your component’s test. It also doesn’t require DOM.