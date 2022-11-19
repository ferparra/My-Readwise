title:: Workflows Are Coming to Supabase (highlights)
author:: [[supabase.io]]
full-title:: "Workflows Are Coming to Supabase"
category:: #articles
url:: https://supabase.io/blog/2021/04/02/supabase-workflows

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Workflows orchestrate and execute functions in response to a database event (insert, update, delete) or a HTTP call (direct invocation).You can use them to rapidly develop microservices (once we have functions) without worrying about servers.Workflows are stateless - the output of a state becomes the input of the next state.Workflows are defined using Amazon States Languages, so you can import your workflows from AWS (although we are still building handlers
	  for most AWS resources).Workflows can be persistent (the default). This means they are tolerant to server restarts, but it also means they need to use
	  the database to store their state.Workers can be transient. These are fully in-memory if you don't want to store the execution state (for example, IoT
	  applications that trigger workflows very often). Transient workflows are not restarted if the server crashes or is restarted.