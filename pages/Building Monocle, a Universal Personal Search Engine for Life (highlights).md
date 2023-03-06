title:: Building Monocle, a Universal Personal Search Engine for Life (highlights)
author:: [[thesephist.com]]
full-title:: "Building Monocle, a Universal Personal Search Engine for Life"
category:: #articles
url:: https://thesephist.com/posts/monocle/
document_note:: Monocle is a search engine that allows users to search all of their personal data such as blog posts, journal entries, contacts, Tweets and more. It is designed to act as an "extended memory" for the user, allowing them to quickly find any information they need in under five seconds from anywhere on their computer. It was built over a weekend with a custom search algorithm and compressed, pre-generated index of its document dataset. Monocle also serves as a proof-of-concept that shows what is possible when users build and manage their own tools and information.
tags:: #[[gpt]] #[[pkm]]

- Highlights first synced by [[Readwise]] [[Feb 25th, 2023]]
	- *effective recall* of information was critical to a good personal knowledge tool ([View Highlight](https://read.readwise.io/read/01gt3avgee490zn8102nn1y8w6))
	- Monocle loads a compressed, pre-generated index of its document dataset on startup, and performs all search locally in the browser. ([View Highlight](https://read.readwise.io/read/01gt3aw9qwtp181gdfpa1mq3w2))
	- Second, **I wanted an indexer and search algorithm that I owned and understood.** This is partly because I just wanted to learn and understand how full-text search engines worked, and the way I learn is often by building tools for myself using that knowledge. Another benefit of a fully custom, from-scratch search algorithm is that if I understand the whole system, I can be aware of its limitations and come back to improve it as I need the algorithm to improve. The “search algorithm” is really a few different parts:
	  
	  1.  the indexer, which catalogues keywords in the indexed documents
	  2.  the searcher, which reads documents from the index to find matching results
	  3.  the stemmer, which expands search queries to include variations of words like “tool” to “tools” or “create” to “creating”
	  4.  the ranker, which is responsible for ordering search results by some measure of relevance. ([View Highlight](https://read.readwise.io/read/01gt3awhd8zd4w264r1m19sf21))
		- **Note**: The goal of building Monocle was to create a universal personal search engine for life, and to do so, the creator wanted to own and understand the indexer and search algorithm. To this end, the algorithm was built from scratch and consists of an indexer to catalogue keywords, a searcher to find matching results, a stemmer to expand search queries, and a ranker to order results by relevance.
	- ![](https://thesephist.com/img/monocle-diagram.jpg) ([View Highlight](https://read.readwise.io/read/01gt3axg33j6j60hznx6720yvc))