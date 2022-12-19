title:: Feature Toggles (highlights)
author:: [[Pete Hodgson]]
full-title:: "Feature Toggles"
category:: #articles
url:: https://martinfowler.com/articles/feature-toggles.html

- Highlights first synced by [[Readwise]] [[Dec 18th, 2022]]
	- Have the Toggle Router make decisions based on a **Toggle Configuration**, and make that configuration environment-specific. Only turn the new feature on in a pre-production environment. ([View Highlight](https://read.readwise.io/read/01gmhkbtq8xn6yxtcpc609ged6))
	- Allow Toggle Configuration to be modified at runtime via some form of admin UI. Use that admin UI to turn the new feature on a test environment. ([View Highlight](https://read.readwise.io/read/01gmhkby48e893grdprhv9g01z))
	- Teach the Toggle Router how to make dynamic, per-request toggling decisions. These decisions take **Toggle Context** into account, for example by looking for a special cookie or HTTP header. Usually Toggle Context is used as a proxy for identifying the user making the request. ([View Highlight](https://read.readwise.io/read/01gmhkc0mk7rsv4czg0xrvw145))
	- ![](https://martinfowler.com/articles/feature-toggles.html/feature-toggles/overview-diagram.png) ([View Highlight](https://read.readwise.io/read/01gmhkc2x1mb1adhn4y8dvth9a))
	- ![](https://martinfowler.com/articles/feature-toggles.html/feature-toggles/chart-1.png) ([View Highlight](https://read.readwise.io/read/01gmhkc83mks41f8p149n6cwt5))
	- ![](https://martinfowler.com/articles/feature-toggles.html/feature-toggles/chart-2.png) ([View Highlight](https://read.readwise.io/read/01gmhkcavn1gfkqkt943fdcz45))
	- ![](https://martinfowler.com/articles/feature-toggles.html/feature-toggles/chart-3.png) ([View Highlight](https://read.readwise.io/read/01gmhkcee9y2hgmbyjzpc2bm8g))
	- ![](https://martinfowler.com/articles/feature-toggles.html/feature-toggles/chart-4.png) ([View Highlight](https://read.readwise.io/read/01gmhkcjk2b2gffvjt0y0dbtcy))
	- ![](https://martinfowler.com/articles/feature-toggles.html/feature-toggles/chart-6.png) ([View Highlight](https://read.readwise.io/read/01gmhkcxcs1j13wcgs004zk1s0))
	- ![](https://martinfowler.com/articles/feature-toggles.html/feature-toggles/chart-5.png) ([View Highlight](https://read.readwise.io/read/01gmhkd0jfam4g9kftqvhehm5p))
	- ![](https://martinfowler.com/articles/feature-toggles.html/feature-toggles/feature-toggles-testing.png) ([View Highlight](https://read.readwise.io/read/01gmhke6brsgje264p7zm0w92g))