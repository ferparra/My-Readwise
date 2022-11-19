title:: Tweets from дэн (highlights)
author:: [[@dan_abramov on Twitter]]
full-title:: "Tweets from дэн"
category:: #tweets
url:: https://twitter.com/dan_abramov

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- react tip: skipping re-renders (eg with memo) is a performance optimization only. if you solved a bug by “avoiding a re-render”, the bug is still there — it’s in your component. re-renders with the same data are supposed to have no noticeable impact at all. ([View Tweet](https://twitter.com/dan_abramov/status/1575553047408902147))
	- 💡 easy way to memorize flexbox:
	- this whole definition style
	  
	  const Button = ({ stuff }) => (
	  <button>...</button>
	  )
	  
	  without writing explicit return was quite an annoying fad. every time you want to add some logic you have to refactor it to braces. glad it seems to (mostly) be over :) ([View Tweet](https://twitter.com/dan_abramov/status/1570426739591114755))