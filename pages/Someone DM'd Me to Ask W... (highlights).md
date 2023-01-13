title:: Someone DM'd Me to Ask W... (highlights)
author:: [[@jitl on Twitter]]
full-title:: "Someone DM'd Me to Ask W..."
category:: #tweets
url:: https://twitter.com/jitl/status/1530326516013342723

- Highlights first synced by [[Readwise]] [[Jan 2nd, 2023]]
	- Someone DM'd me to ask what tech we use in the Notion iOS/Android apps.
	  
	  • They're hybrid native apps – idiomatic Kotlin/Swift + a webview running our web app.
	  • We used React Native back in the day, but removed it by early 2020.
	  • SQLite. ([View Tweet](https://twitter.com/jitl/status/1530326516013342723))
		- **Note**: Thread
	- @TheJemaz @sebastienlorber @SamuelShearing @avohmincevs @BuchAbhay The app should be native speed. Easier to be native speed if actually native. With information and experience we had, knowledge of problem space and constraints, it was a no-brainer to get rid of it ASAP. ([View Tweet](https://twitter.com/jitl/status/1550453762585755648))
	- Our strategy is to progressively nativeify more parts of our app as we grow the team.
	  However, the editor will probably remain a webview for the foreseeable future, because of complexity tradeoff. Google Docs, Quip, Dropbox Paper, Coda - all use native shell, webview editor. https://t.co/394Cw0Nttx ([View Tweet](https://twitter.com/jitl/status/1550522855527292928))