title:: Matrix Multiplication Is... (highlights)
author:: [[@TivadarDanka on Twitter]]
full-title:: "Matrix Multiplication Is..."
category:: #tweets
url:: https://twitter.com/TivadarDanka/status/1592837142211833857

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Matrix multiplication is not easy to understand.
	  
	  Even looking at the definition used to make me sweat, let alone trying to comprehend the pattern. Yet, there is a stunningly simple explanation behind it.
	  
	  Let's pull back the curtain! 
	  
	  ![](https://pbs.twimg.com/media/Fhrk8DEVIAAPQ5w.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1592837142211833857))
		- **Note**: Thread
	- First, the raw definition.
	  
	  This is how the product of A and B is given. Not the easiest (or most pleasant) to look at.
	  
	  We are going to unwrap this. 
	  
	  ![](https://pbs.twimg.com/media/Fhrk8cnUYAEqb4i.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1592837151472766976))
	- Here is a quick visualization before the technical details.
	  
	  The element in the i-th row and j-th column of AB is the dot product of A's i-th row and B's j-th column. 
	  
	  ![](https://pbs.twimg.com/media/Fhrk87FVEAYKRG8.png) ([View Tweet](https://twitter.com/TivadarDanka/status/1592837158624075777))
	- Now, let's look at a special case: multiplying the matrix A with a (column) vector whose first component is 1, and the rest is 0.
	  
	  Let's name this special vector e₁.
	  
	  Turns out that the product of A and e₁ is the first column of A. 
	  
	  ![](https://pbs.twimg.com/media/Fhrk9WOUYAEcFsn.png) ([View Tweet](https://twitter.com/TivadarDanka/status/1592837165452386304))
	- Similarly, multiplying A with a (column) vector whose second component is 1 and the rest is 0 yields the second column of A.
	  
	  That's a pattern! 
	  
	  ![](https://pbs.twimg.com/media/Fhrk9ufUAAEExFj.png) ([View Tweet](https://twitter.com/TivadarDanka/status/1592837171852939265))
	- By the same logic, we conclude that A times eₖ equals the k-th column of A.
	  
	  This sounds a bit algebra-y, so let's see this idea in geometric terms.
	  
	  Yes, you heard right: geometric terms. 
	  
	  ![](https://pbs.twimg.com/media/Fhrk-JQVQAAa5aM.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1592837179482382337))
	- Matrices represent linear transformations. You know, those that stretch, skew, rotate, flip, or otherwise linearly distort the space.
	  
	  The images of basis vectors form the columns of the matrix.
	  
	  We can visualize this in two dimensions. 
	  
	  ![](https://pbs.twimg.com/media/Fhrk-iAVEAMjOZr.png) ([View Tweet](https://twitter.com/TivadarDanka/status/1592837186151251968))
	- Moreover, we can look at a matrix-vector product as a linear combination of the column vectors.
	  
	  Make a mental note of this, because it is important. 
	  
	  ![](https://pbs.twimg.com/media/Fhrk-9FUAAAIL77.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1592837193642299392))
	- (If unwrapping the matrix-vector product seems too complex, I got you.
	  
	  The computation below is the same as in the above tweet, only in vectorized form.) 
	  
	  ![](https://pbs.twimg.com/media/Fhrk_W3VQAACBo1.png) ([View Tweet](https://twitter.com/TivadarDanka/status/1592837200621674496))
	- Now, about the matrix product formula.
	  
	  From a geometric perspective, the product AB is the same as first applying B, then A to our underlying space. 
	  
	  ![](https://pbs.twimg.com/media/Fhrk_0HUUAICVT0.png) ([View Tweet](https://twitter.com/TivadarDanka/status/1592837209769447424))
	- Recall that matrix-vector products are linear combinations of column vectors.
	  
	  With this in mind, we see that the first column of AB is the linear combination of A's columns. (With coefficients from the first column of B.) 
	  
	  ![](https://pbs.twimg.com/media/FhrlAZsVEAADEAG.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1592837218904571904))
	- We can collapse the linear combination into a single vector, resulting in a formula for the first column of AB.
	  
	  This is straight from the mysterious matrix product formula. 
	  
	  ![](https://pbs.twimg.com/media/FhrlA3DVIAEAR7i.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1592837226626310145))
	- The same logic can be applied, thus giving an explicit formula to calculate the elements of a matrix product. 
	  
	  ![](https://pbs.twimg.com/media/FhrlBR6VIAAj57L.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1592837233282646016))
	- Linear algebra is powerful exactly because it abstracts away the complexity of manipulating data structures like vectors and matrices.
	  
	  Instead of explicitly dealing with arrays and convoluted sums, we can use simple expressions AB.
	  
	  That's a huge deal. ([View Tweet](https://twitter.com/TivadarDanka/status/1592837236357111809))
	- Peter Lax sums it up perfectly: "So what is gained by abstraction? First of all, the freedom to use a single symbol for an array; this way we can think of vectors as basic building blocks, unencumbered by components." ([View Tweet](https://twitter.com/TivadarDanka/status/1592837238898900992))
	- Without a doubt, linear algebra is one of the most important mathematical tools for a machine learning practitioner.
	  
	  I wrote the book to get you from high school math to linear algebra mastery. Get your copy now!
	  
	  (Lifetime updates included.)
	  
	  https://t.co/w1Fcybpauh ([View Tweet](https://twitter.com/TivadarDanka/status/1592837241344180224))
	- Read the unrolled thread here:
	  
	  https://t.co/WpbK1UfYwW ([View Tweet](https://twitter.com/TivadarDanka/status/1592837243864985600))
	- If you have enjoyed this explanation, share it with your friends and give me a follow! I regularly post deep-dive explainers such as this. https://t.co/3blZEsJBah ([View Tweet](https://twitter.com/TivadarDanka/status/1592837246448652288))