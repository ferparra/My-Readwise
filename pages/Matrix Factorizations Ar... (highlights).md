title:: Matrix Factorizations Ar... (highlights)
author:: [[@TivadarDanka on Twitter]]
full-title:: "Matrix Factorizations Ar..."
category:: #tweets
url:: https://twitter.com/TivadarDanka/status/1570736015723364352

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Matrix factorizations are the pinnacle results of linear algebra.
	  
	  From theory to applications, they are behind many theorems, algorithms, and methods. However, it is easy to get lost in the vast jungle of decompositions.
	  
	  This is how to make sense of them. 
	  
	  ![](https://pbs.twimg.com/media/FcxgFJRaEAMzqCn.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1570736015723364352))
		- **Note**: Thread
	- We are going to study three matrix factorizations:
	  
	  1. the LU decomposition,
	  2. the QR decomposition,
	  3. and the Singular Value Decomposition (SVD).
	  
	  First, we'll take a look at LU. ([View Tweet](https://twitter.com/TivadarDanka/status/1570736019531763712))
	- 1. The LU decomposition.
	  
	  Let's start at the very beginning: linear equation systems.
	  
	  Linear equations are surprisingly effective in modeling real-life phenomena: economic processes, biochemical systems, etc. 
	  
	  ![](https://pbs.twimg.com/media/FcxgFsoagAMqC_4.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1570736026968289280))
	- To simplify the notation, we can represent linear equations in a matrix form.
	  
	  𝐴 holds the coefficients, 𝑥 holds the solution.
	  
	  How can we solve this? 
	  
	  ![](https://pbs.twimg.com/media/FcxgGK6aMAEmSQm.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1570736034736132097))
	- By multiplying the equations with scalars and subtracting them from each other, we can (usually) transform the system into an upper triangular form.
	  
	  This is called Gaussian elimination.
	  
	  The resulting system is easy to solve: solve the last equation, then move up progressively. 
	  
	  ![](https://pbs.twimg.com/media/FcxgGm4aMAID-U-.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1570736042789187585))
	- As it turns out, Gaussian elimination is equivalent to multiplying 𝐴 by a lower diagonal matrix.
	  
	  This gives the famous LU decomposition, factoring 𝐴 into the product of a lower and an upper diagonal matrix. 
	  
	  ![](https://pbs.twimg.com/media/FcxgHF3aUAEkbIC.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1570736051559485440))
	- Thus, LU is the same as solving a linear equation.
	  
	  The LU decomposition can be performed whenever Gaussian elimination can, and it is vital in many applications, for instance, computing determinants or inverting matrices. ([View Tweet](https://twitter.com/TivadarDanka/status/1570736055015591937))
	- 2. The QR decomposition.
	  
	  There are more than one ways to think about matrices. Previously, we viewed them as linear equations, but we can think about them as a horizontal stack of column vectors. 
	  
	  ![](https://pbs.twimg.com/media/FcxgHwXaMAAPIuz.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1570736062007480321))
	- We can put these column vectors into the Gram-Schmidt orthogonalization process, yielding a set of orthonormal vectors that span the same space. 
	  
	  ![](https://pbs.twimg.com/media/FcxgINIaMAAGExD.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1570736070081531905))
	- Just like Gaussian elimination, the Gram-Schmidt process can also be "vectorized", allowing us to use the resulting orthonormal system to factorize 𝐴 into the product of an orthogonal and an upper diagonal matrix.
	  
	  Voila! This is the gist of QR decomposition. 
	  
	  ![](https://pbs.twimg.com/media/FcxgIr7aIAAidJv.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1570736079103479810))
	- Again, there are tons of applications, but the most significant one is the famous QR algorithm, using the QR decomposition to find the eigenvalues and the eigenvectors of arbitrary matrices.
	  
	  https://t.co/7Ub7sCRqHa ([View Tweet](https://twitter.com/TivadarDanka/status/1570736082249216000))
	- 3. The Singular Value Decomposition.
	  
	  SVD is undoubtedly one of the pinnacle results of linear algebra, omnipresent in computer science and machine learning. For instance, the famous PCA algorithm is a version of SVD. ([View Tweet](https://twitter.com/TivadarDanka/status/1570736085042622467))
	- To understand the SVD, we should view matrices as linear transformations.
	  
	  In essence, a linear transformation is a distortion of the underlying vector space, as illustrated below. 
	  
	  ![](https://pbs.twimg.com/media/FcxgJhKaMAEoVEx.png) ([View Tweet](https://twitter.com/TivadarDanka/status/1570736092760145921))
	- Although linear transformations can be complex, they are built from a few basic building blocks: rotations, reflections, stretchings.
	  
	  A combination of rotations + reflections corresponds to a matrix whose columns are orthogonal.
	  
	  Stretchings correspond to diagonal matrices. ([View Tweet](https://twitter.com/TivadarDanka/status/1570736096094584833))
	- On the level of transformations, SVD says that every transformation is a composition of
	  
	  1. a rotations + reflections combo,
	  2. a stretching,
	  3. and a final rotations + reflections combo,
	  
	  in that order. 
	  
	  ![](https://pbs.twimg.com/media/FcxgKKbaUAAAqPh.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1570736103312982019))
	- Translating it to the language of matrices, we obtain the factorization of 𝐴 into orthogonal and diagonal matrices.
	  
	  This is an extremely strong result. Like the prime factorization theorem of integers, just for matrices.
	  
	  (SVD works for non-square matrices as well.) 
	  
	  ![](https://pbs.twimg.com/media/FcxgKnzacAM7bYZ.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1570736113089933316))
	- SVD is everywhere in linear algebra. For instance, we can
	  
	  1. generalize the notion of the inverse matrix to non-square matrices,
	  2. reduce the dimensionality of data,
	  3. approximate matrices with low-rank ones,
	  
	  and many more. ([View Tweet](https://twitter.com/TivadarDanka/status/1570736116487323648))
	- You can read the unrolled thread here:
	  
	  https://t.co/MLIg1jwzGF ([View Tweet](https://twitter.com/TivadarDanka/status/1570736119238762497))
	- This is just the tip of the iceberg. If you are in more about the beauties of linear algebra, check out my Mathematics of Machine Learning book!
	  
	  Understanding mathematics will make you a better engineer, and I want to help you with that.
	  
	  https://t.co/sqaja6hH92 ([View Tweet](https://twitter.com/TivadarDanka/status/1570736122065735681))