title:: Parcel 2 Beta 3 (highlights)
author:: [[v2.parceljs.org]]
full-title:: "Parcel 2 Beta 3"
category:: #articles
url:: https://v2.parceljs.org/blog/beta3/

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- Another feature related to our scope hoisting implementation is support for tree shaking dynamic import(). Parcel can detect which properties of a dynamic import are accessed, and exclude the exports from the resolved module that aren't used. This works with promise chaining, async/await, destructuring, and static object property accesses.