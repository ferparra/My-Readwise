title:: My General Feeling About... (highlights)
author:: [[@allenholub on Twitter]]
full-title:: "My General Feeling About..."
category:: #tweets
url:: https://twitter.com/allenholub/status/1399047162978357248

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- My general feeling about GraphQL is that a back end that does nothing but get/set data is awful design. Sure, there are occasional uses (e.g. a micro-frontend talking to its server-side counterpart), but outside of that, getters & setters are a hideously bad smell. 1/4 ([View Tweet](https://twitter.com/allenholub/status/1399047160524640265))
		- **Note**: Thread
	- Query languages are not APIs. Remote entities should do things. Their API should tell them what to do. The data should stay put. The only common exception I can immagine is a UI exposed by a backend component. 2/4 ([View Tweet](https://twitter.com/allenholub/status/1399047161279614980))
	- There, the UI is really part of the backend component that happens to be running on a different machine. Conceptually, they’re part of the same "object." 3/4 ([View Tweet](https://twitter.com/allenholub/status/1399047162235924481))
	- If your backend is just a database and you don’t want SQL on the client, well fine, but the backend-as-database is itself a bad smell in most applications. 4/4 ([View Tweet](https://twitter.com/allenholub/status/1399047162978357248))