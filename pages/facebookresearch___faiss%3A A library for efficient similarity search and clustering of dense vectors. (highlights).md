title:: facebookresearch/faiss: A library for efficient similarity search and clustering of dense vectors. (highlights)
author:: [[github.com]]
full-title:: "facebookresearch/faiss: A library for efficient similarity search and clustering of dense vectors."
category:: #articles
url:: https://github.com/facebookresearch/faiss
tags:: #[[ai]] #[[search]] 
![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_5318/faiss)

- Highlights first synced by [[Readwise]] [[Mar 31st, 2023]]
	- Faiss contains several methods for similarity search. It assumes that the instances are represented as vectors and are identified by an integer, and that the vectors can be compared with L2 (Euclidean) distances or dot products. Vectors that are similar to a query vector are those that have the lowest L2 distance or the highest dot product with the query vector. It also supports cosine similarity, since this is a dot product on normalized vectors. ([View Highlight](https://read.readwise.io/read/01gwtdct243netp0pqhxa4t480))
	- Some of the methods, like those based on binary vectors and compact quantization codes, solely use a compressed representation of the vectors and do not require to keep the original vectors. This generally comes at the cost of a less precise search but these methods can scale to billions of vectors in main memory on a single server. Other methods, like HNSW and NSG add an indexing structure on top of the raw vectors to make searching more efficient. ([View Highlight](https://read.readwise.io/read/01gwtdcxgdgzbdm5he32h7gxnq))