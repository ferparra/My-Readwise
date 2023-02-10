title:: Today We Are Announcing... (highlights)
author:: [[@nikitabase on Twitter]]
full-title:: "Today We Are Announcing..."
category:: #tweets
url:: https://twitter.com/nikitabase/status/1623369718735474688

- Highlights first synced by [[Readwise]] [[Feb 9th, 2023]]
	- Today we are announcing @neondatabase integration with @vercel previews which allows you to have a dedicated Postgres environment for every preview. 🧵 ([View Tweet](https://twitter.com/nikitabase/status/1623369718735474688))
		- **Note**: Thread
	- As an industry are moving from staging to previews and modern platforms like @vercel and @github generate previews for every pull request. ([View Tweet](https://twitter.com/nikitabase/status/1623369719930822656))
	- It wasn't possible for databases to "branch" and move data from a production environment to a preview database for each commit until now. ([View Tweet](https://twitter.com/nikitabase/status/1623369721004572672))
	- It's only possible now because of the copy-on-write technology of @neondatabase storage and an incredible partnership between @neondatabase and @vercel ([View Tweet](https://twitter.com/nikitabase/status/1623369722187370497))
	- For each commit @vercel builds a preview and calls into @neondatabase to create a branch which is an instant operation due to the copy-on-write. Then it populates connection details into the preview environment and voila - you have a preview for your whole app ([View Tweet](https://twitter.com/nikitabase/status/1623369723210760192))
	- Staging is dead. Long live previews! https://t.co/58tpEdWkXA ([View Tweet](https://twitter.com/nikitabase/status/1623369724309684224))