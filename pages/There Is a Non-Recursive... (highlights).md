title:: There Is a Non-Recursive... (highlights)
author:: [[@TivadarDanka on Twitter]]
full-title:: "There Is a Non-Recursive..."
category:: #tweets
url:: https://twitter.com/TivadarDanka/status/1622922634907488256

- Highlights first synced by [[Readwise]] [[Feb 9th, 2023]]
	- There is a non-recursive formula for the Fibonacci numbers, expressing them in terms of the golden ratio and its powers.
	  
	  Why should you be interested? For one, because it teaches an extremely valuable lesson about power series.
	  
	  Read on to find out what. 
	  
	  ![](https://pbs.twimg.com/media/FoXHiD7aMAEfwgx.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1622922634907488256))
		- **Note**: Thread
	- The Fibonacci numbers form one of the most famous integer sequences, known for their intimate connection to the golden ratio, sunflower spirals, mating habits of rabbits, and several other things.
	  
	  By definition, they are defined by a simple second-order recursion. 
	  
	  ![](https://pbs.twimg.com/media/FoXHiloakAMp9OQ.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1622922643895914496))
	- What’s usually not known is that the Fibonacci numbers have a simple and beautiful closed-form expression, written in terms of the golden ratio.
	  
	  This is called the Binet formula. In this thread, we are going to derive it from the first principles. ([View Tweet](https://twitter.com/TivadarDanka/status/1622922647553343488))
	- Let's start with our primary tool: power series.
	  
	  A power series is an infinite sum of monomials. You can think about them as “polynomials of infinite degree”. The coefficients of the monomials are called the coefficients of the power series. 
	  
	  ![](https://pbs.twimg.com/media/FoXHjPraIAAxpPp.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1622922656667549697))
	- One of the most important examples is the famous geometric series.
	  
	  We’ll use this to derive the closed formula for the Fibonacci numbers. 
	  
	  ![](https://pbs.twimg.com/media/FoXHj17aEAEVAFJ.png) ([View Tweet](https://twitter.com/TivadarDanka/status/1622922665186193408))
	- A power series is fully determined by its coefficients: two power series are equal if and only if their coefficients are equal. This is called the uniqueness property of power series. 
	  
	  ![](https://pbs.twimg.com/media/FoXHkUhaYAAVgpb.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1622922675210571776))
	- Power series are also linear in a sense. That is, summing two power series is the same as summing their coefficients. 
	  
	  ![](https://pbs.twimg.com/media/FoXHk6TaAAAWvCN.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1622922684421259264))
	- What happens if we define a power series via the Fibonacci numbers? Let’s find out. This is called the Fibonacci generating function. 
	  
	  ![](https://pbs.twimg.com/media/FoXHldVacAAZshr.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1622922694424670213))
	- First, we’ll use the recursion to obtain a closed-form expression for F(x).
	  
	  Do you recall how the Fibonacci numbers were initially defined? We can multiply each term with the corresponding monomial to obtain the terms of the generating function on both sides. 
	  
	  ![](https://pbs.twimg.com/media/FoXHmCJakAIrhYx.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1622922703685713923))
	- After summing the terms, we obtain an equation - for the generating function! 
	  
	  ![](https://pbs.twimg.com/media/FoXHmkCagAEcJMK.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1622922713110319105))
	- With a tiny bit of algebra, we can find the closed form of F(x)! Here it is below. 
	  
	  ![](https://pbs.twimg.com/media/FoXHnH5akAA_9dt.png) ([View Tweet](https://twitter.com/TivadarDanka/status/1622922721830260736))
	- The right-hand side is a rational fraction, that is, the fraction of two polynomials.
	  
	  How are we going to find the power series for this particular rational fraction? By taking a closer look at the polynomial 1 - x - x² in the denominator. ([View Tweet](https://twitter.com/TivadarDanka/status/1622922725240209410))
	- The second-degree polynomial 1 - x - x² is a famous one. Why? Let’s take a look at its roots via the quadratic formula. 
	  
	  ![](https://pbs.twimg.com/media/FoXHnxFaIAYuCBS.png) ([View Tweet](https://twitter.com/TivadarDanka/status/1622922732618027010))
	- This is the golden ratio and its conjugate! 
	  
	  ![](https://pbs.twimg.com/media/FoXHoRBaYAAHOeg.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1622922742319439872))
	- These two numbers are quite special. Geometrically speaking, they describe the segments a and b such that the ratio of a to b is the same as a to a + b. 
	  
	  ![](https://pbs.twimg.com/media/FoXHoy7akAQOtnZ.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1622922751077150720))
	- Besides its geometric properties, the golden ratio and its conjugate are also special in an algebraic way. Their sum and product are 1 and -1 respectively, while their difference is √5. 
	  
	  ![](https://pbs.twimg.com/media/FoXHpVWaAAEEoNw.png) ([View Tweet](https://twitter.com/TivadarDanka/status/1622922760522694659))
	- Take note of these, as they’ll come in shortly.
	  
	  What can we do with all of these? As the golden ratio and its conjugate are the roots of 1 - x - x², we can decompose this quadratic polynomial into the product of two linear terms.
	  
	  How? Via the partial fraction decomposition. 
	  
	  ![](https://pbs.twimg.com/media/FoXHp3EaAAE4kit.png) ([View Tweet](https://twitter.com/TivadarDanka/status/1622922769225883648))
	- We love rational fractions for one main reason: because they can be decomposed into the sum of geometric series.
	  
	  In the case of the Fibonacci generating function, the decomposition is particularly simple. 
	  
	  ![](https://pbs.twimg.com/media/FoXHqX8aUAAx4eT.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1622922778419798016))
	- We can find a and b by adding the two fractions together. 
	  
	  ![](https://pbs.twimg.com/media/FoXHq7-aUAARWs2.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1622922787999612930))
	- Using the fact that two polynomials are equal if and only if their coefficients are equal leads to a simple system of linear equations. 
	  
	  ![](https://pbs.twimg.com/media/FoXHre_aMAEJ5oM.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1622922797776510976))
	- This can be easily solved in terms of the golden ratio and its conjugate. 
	  
	  ![](https://pbs.twimg.com/media/FoXHsDlaEAIPfHk.png) ([View Tweet](https://twitter.com/TivadarDanka/status/1622922806957858817))
	- Applying this to the Fibonacci generating function, we can obtain its final form. (Recall that addition and scalar multiplication of power series can be done coefficientwise.) 
	  
	  ![](https://pbs.twimg.com/media/FoXHskNaIAApEH1.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1622922816319545344))
	- And thus, we finally obtain the Binet formula! (As follows from the uniqueness property of power series.) 
	  
	  ![](https://pbs.twimg.com/media/FoXHtIyacAAk5nK.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1622922826448777216))
	- Read the full thread here:
	  
	  https://t.co/QCH1oUa2i8 ([View Tweet](https://twitter.com/TivadarDanka/status/1622922830114607105))
	- If you have enjoyed this thread, follow me and subscribe to my newsletter!
	  
	  Understanding mathematics is a superpower, and I regularly post deep-dive explanations about seemingly complex concepts from math, engineering, and science.
	  
	  https://t.co/uZuKaeHCL1 ([View Tweet](https://twitter.com/TivadarDanka/status/1622922832744435712))