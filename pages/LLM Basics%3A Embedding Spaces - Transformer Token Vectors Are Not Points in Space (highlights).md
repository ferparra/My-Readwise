title:: LLM Basics: Embedding Spaces - Transformer Token Vectors Are Not Points in Space (highlights)
author:: [[NickyP]]
full-title:: "LLM Basics: Embedding Spaces - Transformer Token Vectors Are Not Points in Space"
category:: #articles
url:: https://www.lesswrong.com/posts/pHPmMGEMYefk9jLeh/llm-basics-embedding-spaces-transformer-token-vectors-are
document_note:: The text explains that while token vectors are stored as n-dimensional vectors, they should not be thought of as points in vector space due to the way probabilities of tokens are calculated and the behaviour of the softmax function which affects how tokens are positioned in their space. Instead, the token vectors should be thought of as directions on a (n-1)-hypersphere, with lengths showing how "large" the targets are on a hypersphere. The text also explains the process of how token IDs are converted into vectors and how vectors can be unembedded to get back the original token.

- Highlights first synced by [[Readwise]] [[Mar 16th, 2023]]
	- **TL;DR:** While the token vectors are stored as n-dimensional vectors, thinking of them as points in vector space can be quite misleading. It is better to think of them as directions on a hypersphere, with a size component.
	  
	  The I think of distance as the Euclidean distance, with formula:
	  
	  d(→x1,→x2)=|→x1−→x2|=√∑i(x1i−x2i)2
	  
	  Thus does not match up with the distance forumla used when calculating logits:
	  
	  d(→x1,→x2)=→x1⋅→x2=|→x1||→x2|cosθ12
	  
	  But it does match up with the cosine similarity forumula:
	  
	  d(→x1,→x2)=^x1⋅^x2=cosθ12
	  
	  And so, we can see that the direction and size matter, but not the distance ([View Highlight](https://read.readwise.io/read/01gvjcq252j8wffkcvf9ept47z))
		- **Note**: The way we store tokens as vectors in a computer is different than how we would think of them as points in a space. It is better to think of them as directions on a special shape called a hypersphere, which also has a size component. The formula for Euclidean distance (which shows how far apart two points are) does not work here, but the formula for cosine similarity (which shows how similar two directions are) does. This means that the direction and size of the token vectors matter, but not the distance between them.
	- ![](https://res.cloudinary.com/lesswrong-2-0/image/upload/v1675798520/mirroredImages/pHPmMGEMYefk9jLeh/fwresq3nbxa4r3cgnei2.png) ([View Highlight](https://read.readwise.io/read/01gvjcrzgkgxe17ycvvpb2zrzp))