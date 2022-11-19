title:: Server-Side Tagging in Google Tag Manager (highlights)
author:: [[simoahava.com]]
full-title:: "Server-Side Tagging in Google Tag Manager"
category:: #articles
url:: https://www.simoahava.com/analytics/server-side-tagging-google-tag-manager/

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Server-side tagging has the potential to overturn the current dynamic of data collection and governance for an organization
	- You can run a fully functional digital analytics and marketing setup without loading any third-party code in the user’s browser or device. With appropriate monitoring in place, you can say goodbye to PII and credential leaks, cross-site tracking traps, and bloated third-party JavaScript encumbering the client.
	- the purpose of this setup is to create an endpoint in a server environment that you own. It will act as a sort of a proxy between the hits sent from browsers and devices and the actual endpoints to which the hits are collected.
	- this endpoint would be mapped with a custom subdomain in the same domain hierarchy as the website sending the requests. That way the requests are considered to happen in first-party context, which has a significant impact on how cookies can be read and written
	- an endpoint like google-analytics.com could well be targeted by the heuristics used in content blockers, but my-server-side.domain.com probably isn’t.