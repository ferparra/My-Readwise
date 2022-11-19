title:: CSV Reader Benchmarks: Julia Reads CSVs 10-20x Faster Than Python and R | Hacker News (highlights)
author:: [[news.ycombinator.com]]
full-title:: "CSV Reader Benchmarks: Julia Reads CSVs 10-20x Faster Than Python and R | Hacker News"
category:: #articles
url:: https://news.ycombinator.com/item?id=24746057

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- Producing concrete objects representing every row (e.g. tuples of strings) will always be slower because of the pressure it puts on the heap and memory. Storing 10 million rows with 10 cols of 8-byte floats in an array might only generate 800 MB of memory bandwidth, the equivalent concrete list-of-floats PyObjects would come out at 6160 MB bandwidth and a ton of CPU burned in the allocator. There are use cases where either representation is preferred, and using e.g. PyArrow's parser then simply iterating the result as concrete objects, worst case the result will be slower than directly decoding to PyObject to begin with.
	- Lumping floating point decoding (a problem with large performance-correctness tradeoffs) in with CSV parsing. It's hard to decode floats both quickly and precisely, it's also impractical to describe in the context of a comparison of CSV parsers which language/implementation might decode floats better and why that is better.