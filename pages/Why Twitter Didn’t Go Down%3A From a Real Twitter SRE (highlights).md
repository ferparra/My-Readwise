title:: Why Twitter Didn’t Go Down: From a Real Twitter SRE (highlights)
author:: [[matthewtejo.substack.com]]
full-title:: "Why Twitter Didn’t Go Down: From a Real Twitter SRE"
category:: #articles
url:: https://matthewtejo.substack.com/p/why-twitter-didnt-go-down-from-a

- Highlights first synced by [[Readwise]] [[Nov 23rd, 2022]]
	- One more nice thing Aurora and Mesos does for us is ensure that not too many applications will be put on a single rack. So the whole rack can go down safely and suddenly, Aurora and Mesos will find new servers to be homes for the applications that were running there.