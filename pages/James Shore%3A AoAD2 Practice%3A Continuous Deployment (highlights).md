title:: James Shore: AoAD2 Practice: Continuous Deployment (highlights)
author:: [[jamesshore.com]]
full-title:: "James Shore: AoAD2 Practice: Continuous Deployment"
category:: #articles
url:: https://www.jamesshore.com/v2/books/aoad2/continuous_deployment

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- Done correctly, continuous integration means that the team is ready to release at any time. You’ve tested your code and exercised your deployment scripts.
	- by deploying small pieces frequently, we reduce the risk that a big change will cause problems, and we make it easy to find and fix problems when they do occur.
	- To reduce the impact of failure, deploy to a subset of servers, called canary servers, and automatically compare metrics from the old deploy to the new deploy.
	- For large or risky changes, consider running the code in production, without revealing it to users, before you release. This will allow you to validate its performance and stability.
	- Separating data migration from deployment allows each deploy to fail, and be rolled back, without losing any data. The data migration only happens once the new code has proven to be stable in production.
	- Migrations involving large amount of data require special care, because the production system needs to remain available while the data is migrating.