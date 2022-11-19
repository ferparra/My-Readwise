title:: What Is Server-Driven UI? - Judo (highlights)
author:: [[judo.app]]
full-title:: "What Is Server-Driven UI? - Judo"
category:: #articles
url:: https://www.judo.app/blog/server-driven-ui/

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- The downside to this approach is that the user interface must be fetched every time the listing screen is viewed. The user is presented with a blank screen and shown a loading indicator while waiting for the UI and data from the server. This is a step backwards from the traditional approach where the UI is embedded in the app and users never have to wait for it to load.
	- An alternative way to implement SDUI, and the one that Judo uses, is to separate fetching the user interface and fetching the data into two phases. This has a dramatic reduction in the server response sizes for list views as the presentation markup doesn’t need to be repeated for each item.
	- SDUI customizes the user interface of your app based on the response from a server but it does not change the code.