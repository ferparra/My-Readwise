title:: RecursiveCharacterTextSplitter (highlights)
author:: [[langchain.com]]
full-title:: "RecursiveCharacterTextSplitter"
category:: #articles
url:: https://python.langchain.com/en/latest/modules/indexes/text_splitters/examples/recursive_text_splitter.html
tags:: #[[LLMs]]

- Highlights first synced by [[Readwise]] [[Apr 7th, 2023]]
	- This text splitter is the recommended one for generic text. It is parameterized by a list of characters. It tries to split on them in order until the chunks are small enough. The default list is `["\n\n", "\n", " ", ""]`. This has the effect of trying to keep all paragraphs (and then sentences, and then words) together as long as possible, as those would generically seem to be the strongest semantically related pieces of text. ([View Highlight](https://read.readwise.io/read/01gxcfz6z46n26gpjeqrcr2szb))