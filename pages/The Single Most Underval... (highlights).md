title:: The Single Most Underval... (highlights)
author:: [[@TivadarDanka on Twitter]]
full-title:: "The Single Most Underval..."
category:: #tweets
url:: https://twitter.com/TivadarDanka/status/1502215264544296962

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- The single most undervalued fact of linear algebra: matrices are graphs, and graphs are matrices.
	  
	  Encoding matrices as graphs is a cheat code, making complex behavior simple to study.
	  
	  Let me show you how! 
	  
	  ![](https://pbs.twimg.com/media/FNjw0icVEAUpZcb.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1502215264544296962))
		- **Note**: Thread
	- If you looked at the example above, you probably figured out the rule.
	  
	  Each row is a node, and each element represents a directed and weighted edge.
	  
	  The element in the 𝑖-th row and 𝑗-th column corresponds to an edge going from 𝑖 to 𝑗. ([View Tweet](https://twitter.com/TivadarDanka/status/1502215268247896065))
	- Why is the directed graph representation beneficial for us?
	  
	  For one, the powers of the matrix correspond to walks in the graph.
	  
	  Take a look at the elements of the square matrix. All possible 2-step walks are accounted for in the sum defining the elements of A². 
	  
	  ![](https://pbs.twimg.com/media/FNjw1EQVQAQR349.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1502215274954514434))
	- If the directed graph represents the states of a Markov chain, the square of its transition probability matrix essentially shows the probability of the chain having some state after two steps. ([View Tweet](https://twitter.com/TivadarDanka/status/1502215278868201474))
	- There is much more to this connection.
	  
	  For instance, it gives us a deep insight into the structure of nonnegative matrices.
	  
	  To see what graphs show about matrices, let's talk about the concept of strongly connected components. ([View Tweet](https://twitter.com/TivadarDanka/status/1502215281791287297))
	- A directed graph is strongly connected if every node can be reached from every other node.
	  
	  Below, you can see two examples where this holds and doesn't hold. 
	  
	  ![](https://pbs.twimg.com/media/FNjw112VkAAeJiX.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1502215288036548608))
	- Matrices that correspond to strongly connected graphs are called irreducible. All other nonnegative matrices are called reducible. Soon, we'll see why.
	  
	  (For simplicity, I assumed each edge to have unit weight, but each weight can be an arbitrary nonnegative number.) 
	  
	  ![](https://pbs.twimg.com/media/FNjw2NiVEAI0MLQ.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1502215294198042626))
	- Back to the general case!
	  
	  Even though not all directed graphs are strongly connected, we can partition the nodes into strongly connected components. 
	  
	  ![](https://pbs.twimg.com/media/FNjw2kgVUAE8qUa.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1502215300573401088))
	- Let's label the nodes of this graph and construct the corresponding matrix!
	  
	  (For simplicity, assume that all edges have unit weight.)
	  
	  Do you notice a pattern? 
	  
	  ![](https://pbs.twimg.com/media/FNjw28fVEAEKYe0.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1502215307191984130))
	- The corresponding matrix of our graph can be reduced to a simpler form.
	  
	  Its diagonal comprises blocks whose graphs are strongly connected. (That is, the blocks are irreducible.) Furthermore, the block below the diagonal is zero. 
	  
	  ![](https://pbs.twimg.com/media/FNjw3W-VgAA5wwR.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1502215314737565702))
	- In general, this block-matrix structure is called the Frobenius normal form. 
	  
	  ![](https://pbs.twimg.com/media/FNjw3xHVUAE8_Sb.png) ([View Tweet](https://twitter.com/TivadarDanka/status/1502215320999641091))
	- Let's reverse the question: can we transform an arbitrary nonnegative matrix into the Frobenius normal form?
	  
	  Yes, and with the help of directed graphs, this is much easier to show than purely using algebra. ([View Tweet](https://twitter.com/TivadarDanka/status/1502215324145315840))
	- We have already seen the proof:
	  
	  1. construct the corresponding directed graph,
	  2. find its strongly connected components,
	  3. and renumber its nodes such that the components' nodes form blocks among the integers. ([View Tweet](https://twitter.com/TivadarDanka/status/1502215326947164162))
	- Without going into the details, renumbering the nodes is equivalent to reordering the rows and the columns of our original matrix, resulting in the Frobenius normal form. 
	  
	  ![](https://pbs.twimg.com/media/FNjw4dcUcAAU6Vj.png) ([View Tweet](https://twitter.com/TivadarDanka/status/1502215333297332226))
	- This is just the tip of the iceberg. For example, with the help of matrices, we can define the eigenvalues of graphs!
	  
	  Utilizing the relation between matrices and graphs has been extremely profitable for both graph theory and linear algebra. ([View Tweet](https://twitter.com/TivadarDanka/status/1502215336434679817))
		- **Tags**: #[[favorite]]
	- If you have enjoyed this thread, share it with your friends and follow me!
	  
	  I regularly post deep-dive explanations about seemingly complex concepts from mathematics and machine learning.
	  
	  Understanding math will make you a better engineer, and I want to show you how. ([View Tweet](https://twitter.com/TivadarDanka/status/1502215339291004928))