title:: TeamCity UI: How Do We Test It (highlights)
author:: [[Denis.Lesnik]]
full-title:: "TeamCity UI: How Do We Test It"
category:: #articles
url:: https://blog.jetbrains.com/teamcity/2020/06/teamcity-ui-how-do-we-test-it/

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- Of course, there are also unit tests. It’s simple: we write pure atomic functions and then assert their output. If the output is OK, TeamCity marks them green and allows the pipeline to continue.