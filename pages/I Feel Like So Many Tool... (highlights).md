title:: I Feel Like So Many Tool... (highlights)
author:: [[@geoffreylitt on Twitter]]
full-title:: "I Feel Like So Many Tool..."
category:: #tweets
url:: https://twitter.com/geoffreylitt/status/1516904903184060416

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- I feel like so many tools for "building interactive apps in a spreadsheet" end up struggling w/ the same problem: how to fit side effects and async computations into the simple spreadsheet model of reactivity. 1/ ([View Tweet](https://twitter.com/geoffreylitt/status/1516904903184060416))
		- **Note**: Thread
	- The spreadsheet model is awesome: data updates, pure formulas re-evaluate, the whole sheet is consistent, nice.
	  
	  But what happens when a cell can "do something" when it updates? 2/ ([View Tweet](https://twitter.com/geoffreylitt/status/1516904904538738688))
	- You can try to fit it more closely into the existing spreadsheet model, or you can bolt on an events/triggers system... these days I tend to think a separate event system is more straightforward. Jotted some notes on different approaches: 3/
	  
	  https://t.co/0LJzIzdeiS ([View Tweet](https://twitter.com/geoffreylitt/status/1516904905662816256))
	- Asynchrony is also tricky. Even if your computation is pure, if it's slow and async then you have two options:
	  
	  a) refreshing the spreadsheet is slow
	  b) you can partially refresh the spreadsheet, now the sheet is no longer guaranteed consistent at any given time 🙀
	  
	   4/ ([View Tweet](https://twitter.com/geoffreylitt/status/1516904907030228992))
	- Feels like many of the challenges in UI and state management frameworks boil down to answering these kinds of questions. UI is hard... 5/5 ([View Tweet](https://twitter.com/geoffreylitt/status/1516904908196175872))
	- A classic thorn in the side of a simple reactivity approach: how to handle debounce?
	  
	  Debouncing eliminates the analogy of "one consistent view of now", and forces time into the picture. Naturally takes you from "spreadsheet" to "stream" kind of thinking ([View Tweet](https://twitter.com/geoffreylitt/status/1516905304071434240))
	- Streams are neat when you need them, but seem like overkill in many cases. It's good that spreadsheets don't expose stream analogies
	  
	  https://t.co/LNBusq0lCz ([View Tweet](https://twitter.com/geoffreylitt/status/1516905477048717312))