title:: The Tile Encoder - Exploring ANN Algorithms Part 2.2 (highlights)
author:: [[Abdel Rodriguez]]
full-title:: "The Tile Encoder - Exploring ANN Algorithms Part 2.2"
category:: #articles
url:: https://weaviate.io/blog/ann-algorithms-tiles-enocoder

- Highlights first synced by [[Readwise]] [[Apr 7th, 2023]]
	- While KMeans gives very good results, there are a couple of drawbacks. Firstly, it is expensive to fit to data. Secondly, when compressing vectors, it needs to calculate distances to all centroids for each segment. This results in long encoding and indexing times. ([View Highlight](https://read.readwise.io/read/01gx9sjpfp1qxf1stfv8cz3zct))
	- KMeans produces a tiling over the full range of values using the centroids. Each centroid has a tile associated with it. When a new vector has to be encoded, the algorithm checks which tile it belongs to, and the vector code is set using the index of the closest found tile. When fitting KMeans to our data the generation of the tiles is not homogeneous. As a result, we expect more tiles where there is a higher density of data. This way the data will be balanced over the centroids. ([View Highlight](https://read.readwise.io/read/01gx9sjtw9ffx70qvqgv2kd1e9))
	- Conclusions[​](https://weaviate.io/blog/ann-algorithms-tiles-enocoder#conclusions)
	  
	  In this post we introduced the Tile encoder, an alternative to the KMeans encoder that we mentioned in our last post. Some of the key take away points are that:
	  
	  •   The recall results are very similar when using KMeans vs Tile encoder.
	  •   You need to provide the distribution of your data when using the Tile encoder.
	  •   Fitting with Tile is immediate while it takes much longer with KMeans.
	  •   No downtime when compressing with the Tile encoder, while your server will not be available for querying while compressing with the KMeans encoder.
	  •   You could have the same indexing time when using the Tile encoder if you have enough memory when indexing your data. ([View Highlight](https://read.readwise.io/read/01gx9skfhngpsvgeajraq7fzqf))