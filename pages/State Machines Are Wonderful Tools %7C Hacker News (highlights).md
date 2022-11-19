title:: State Machines Are Wonderful Tools | Hacker News (highlights)
author:: [[news.ycombinator.com]]
full-title:: "State Machines Are Wonderful Tools | Hacker News"
category:: #articles
url:: https://news.ycombinator.com/item?id=25601821

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- There are a couple benefits that come to mind with respect to writing UI. First, it forces you think through all the potential "inputs" on your system, be they button presses from users or network request responses. You have to be explicit about what could have an effect on the system. Secondly, it makes your business logic easier to reason about because you essentially turn your UI code into a bunch of functional statements. All your transitions are just pure functions where the input is the previous state and some input, and the output is the new state.