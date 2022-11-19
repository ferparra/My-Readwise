title:: React, Reselect and Redux (highlights)
author:: [[Dan Parker]]
full-title:: "React, Reselect and Redux"
category:: #articles
url:: https://medium.com/p/b34017f8194c

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- In Redux, whenever an action is called anywhere in the application, all mounted & connected components call their mapStateToProps function. This is why Reselect is awesome. It will just return the memoized result if nothing has changed.