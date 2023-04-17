title:: I Remember Reading About... (highlights)
author:: [[@pikuma on Twitter]]
full-title:: "I Remember Reading About..."
category:: #tweets
url:: https://twitter.com/pikuma/status/1646984400620355590

- Highlights first synced by [[Readwise]] [[Apr 15th, 2023]]
	- I remember reading about determinants in high school. The name was scary and not much context was given. 😦
	  
	  For a long time, a determinant was just a value I had to blindly compute using a formula.
	  
	  Here's what I would like to know about determinants when I first started...  🧵 https://t.co/Q9dOWHQwy2 ([View Tweet](https://twitter.com/pikuma/status/1646984400620355590))
		- **Note**: Thread
	- The word "determinant" appears when we are learning about matrices.
	  
	  And since we want to build some *intuition*, let's look at a simple 2x2 matrix first.
	  
	  We learn that the determinant of a 2x2 matrix is:
	  
	  | a  b |
	  | c  d |  =  a*d - b*c
	  
	  But where does that come from? 
	  
	  ![](https://pbs.twimg.com/media/FtsaVRPWIBIBJux.jpg) ([View Tweet](https://twitter.com/pikuma/status/1646984403153813506))
	- Alright, let's go back in time!
	  
	  Seki Kōwa was a Japanese mathematician from the Edo period. He had Samurai origins but was adopted into the noble Seki family, subject of the shōgun.
	  
	  As a kid, he had great potential with numbers. He was often called "Japan's Newton". 
	  
	  ![](https://pbs.twimg.com/media/FtsbUwjWIBgpybD.jpg) ([View Tweet](https://twitter.com/pikuma/status/1646984405712531456))
	- Seki Kōwa was involved in feudal accounting and also surveying reliable maps for his employer's land.
	  
	  In 1684, his job required him to start looking at *linear systems*.
	  
	  A linear system is a set of *linear* equations that need to be true together (as a system). 
	  
	  ![](https://pbs.twimg.com/media/FtsbsozWIBM8gKR.png) ([View Tweet](https://twitter.com/pikuma/status/1646984412028973060))
	- Oh, and just to make sure we are all on the same page, linear equations are equations that represent functions with solutions that form a line in the Euclidean plane.
	  
	  We put these equations in a system when they all need to hold true at the same time. 
	  
	  ![](https://pbs.twimg.com/media/FtscKwlWIA8OX3a.jpg) ([View Tweet](https://twitter.com/pikuma/status/1646984414629330949))
	- In the example above... a, b, c, d, e, and f are known numbers (usually ∈ ℝ).
	  
	  What we are really interested in is finding the values of (x) and (y) that satisfy that system, making the equality true, together. 
	  
	  ![](https://pbs.twimg.com/media/FtscvfOXoAAerEc.png) ([View Tweet](https://twitter.com/pikuma/status/1646984417884385280))
	- This was how Seki Kōwa approached this problem: 
	  
	  We'll try finding the value of x first.
	  
	  From algebra, we know that we can multiply both sides of the equation by the same value and the equality is still true.
	  
	  Therefore, we're going to multiply the entire first equation by d. 
	  
	  ![](https://pbs.twimg.com/media/FtsdGhaWIBAzMjZ.jpg) ([View Tweet](https://twitter.com/pikuma/status/1646984420392423427))
	- And now, we are going to also multiply the entire second equation by b.
	  
	  Look... I know this looks weird and random, but keep in mind that the main reason we are doing this is because we are trying to cancel the "y" terms out from the final solution so we can find "x". 
	  
	  ![](https://pbs.twimg.com/media/FtsdlsMWIAgdsva.png) ([View Tweet](https://twitter.com/pikuma/status/1646984423760621569))
	- And here is the magic!
	  
	  We will *subtract* both equations, which will hopefully cancel the "y" terms out.
	  
	  We get the result: adx-cbx = de-bf 
	  
	  ![](https://pbs.twimg.com/media/Ftsd-2hWIB8AMXy.jpg) ([View Tweet](https://twitter.com/pikuma/status/1646984427686490113))
	- Now that we canceled the y term out and we have only x left, let's go ahead and find our x.
	  
	  Using simple algebra, if we factor x out on the left side, and then divide everything by (ad-cb), we find our x. 
	  
	  ![](https://pbs.twimg.com/media/FtseTuDWIBkMpU7.jpg) ([View Tweet](https://twitter.com/pikuma/status/1646984430555222017))
	- Cool... do you see how x is written as a fraction?
	  
	  Here comes the most important part of this post...
	  
	  Do you agree that we might have an issue if the denominator (bottom part) of this fraction is *zero*?
	  
	  Therefore, (ad*cb) "DETERMINES" something about our system!!! 
	  
	  ![](https://pbs.twimg.com/media/Ftsemo1WIAso1WH.jpg) ([View Tweet](https://twitter.com/pikuma/status/1646984434107969543))
	- Let me repeat that again!
	  
	  That denominator of this fraction is the "DETERMINANT" that *determines* if we might have a problem when solving our system.
	  
	  Therefore, it is a #determinant of that system. 
	  
	  ![](https://pbs.twimg.com/media/FtsfQRUWIBgLtOK.jpg) ([View Tweet](https://twitter.com/pikuma/status/1646984437887029248))
	- Let's write this down:
	  
	  1. If the denominator is different than zero, we have no problem (and the system has a unique solution).
	  
	  2. If the denominator is zero, we'll have a problem finding a solution for that system.
	  
	  It all depends on the *determinant* of that system! ([View Tweet](https://twitter.com/pikuma/status/1646984439812050944))
	- Independently, in 1693 (about 10 years after Seki Kōwa's discovery), Gottfried Leibniz proposed something similar in a letter that he wrote to the French mathematician l'Hopital. 
	  
	  ![](https://pbs.twimg.com/media/Ftsfv8iWIBcuvSs.jpg) ([View Tweet](https://twitter.com/pikuma/status/1646984442127302657))
	- Seki Kōwa and Leibniz discovered it, but it was Carl Gauss who first used the name "determinant" in 1801.
	  
	  Oh, this intuition behind the determinant of 2x2 system is the same for other dimensions.
	  
	  Of course, the bigger the matrix, the trickier the determinant gets. 
	  
	  ![](https://pbs.twimg.com/media/Ftso26QWAAIu1l2.jpg) ([View Tweet](https://twitter.com/pikuma/status/1646984444295692288))
	- Historically, this is how the word *determinant* first appeared. Of course, there are more modern interpretations of what a determinant is, depending on the context we are using them.
	  
	  This tweet made me think of #gamedev applications of determinants:
	  https://t.co/FXXiloR4J4 ([View Tweet](https://twitter.com/pikuma/status/1646984446271184898))
	- For example, we use a geometrical interpretation of a determinant in our lectures on #GamePhysics.
	  
	  We can realize that the determinant of a 2x2 matrix is the *area of the parallelogram* defined by the vectors of our matrix.
	  
	  Once again, if that area is zero... no bueno! 
	  
	  ![](https://pbs.twimg.com/media/Ftsr85nWcAAka-T.jpg) ([View Tweet](https://twitter.com/pikuma/status/1646984448980680705))
	- Just to give you an example, let's look at how we used the value of a matrix #determinant in our recent Youtube video about "triangle rasterization":
	  
	  📽️https://t.co/qXflKogEk7
	  
	  We must identify and only paint the pixels that are considered to be "inside" a triangle... https://t.co/2fmaFwfwPb ([View Tweet](https://twitter.com/pikuma/status/1646984451551887363))
	- For that, I spoke about an important concept called the "3D vector cross-product".
	  
	  The 3D cross product gives us as a result a new vector that is *perpendicular* (90 degrees) to both vectors A and B. 
	  
	  ![](https://pbs.twimg.com/media/Fts4buFX0Bo3euR.jpg) ([View Tweet](https://twitter.com/pikuma/status/1646984455096082435))
	- And, bear with me for a second because this cross-product conversation has *everything* to do with our talk about determinants!
	  
	  So, one of the problems we had to solve when we were rasterizing our triangle was to compute the total *area* of our 2D triangle on the screen. 
	  
	  ![](https://pbs.twimg.com/media/Fts8z6-WIAELtlX.png) ([View Tweet](https://twitter.com/pikuma/status/1646984457545457667))
	- And for that, we used an important property of the cross-product that tells us that:
	  
	  "The *length* of the perpendicular 3D cross-product vector is also the signed area of the parallelogram formed by the vectors A and B." https://t.co/ktueMUpPpx ([View Tweet](https://twitter.com/pikuma/status/1646984460167004164))
	- So, we can find the area of our screen triangle by computing the cross-product of vectors A and B (edges of our triangle).
	  
	  After all, the cross-product magnitude (length) is the area of the parallelogram, and the area of our triangle is 1/2 of the area of that parallelogram. 
	  
	  ![](https://pbs.twimg.com/media/Fts_e9JWcAIg7_J.jpg) ([View Tweet](https://twitter.com/pikuma/status/1646984462406946816))
	- It looks good, but there is just one catch here!
	  
	  Vector cross-product is only really defined in 3-dimensions... but we can use a small hack to find the "2D cross-product" two vectors.
	  
	  We can *imagine* that there's an arrow perpendicular to the screen, and compute its magnitude. 
	  
	  ![](https://pbs.twimg.com/media/FttAwlkWIAA45nW.jpg) ([View Tweet](https://twitter.com/pikuma/status/1646984464843636739))
	- So, this 2D cross-product is the magnitude (length) of the z-component of the perpendicular vector between A and B.
	  
	  And the z-component of A x B is given by:
	  
	  (a.x*b.y) - (b.x*a.y)
	  
	  Does that look familiar??? 😮
	  
	  That's the formula of the determinant of a 2x2 matrix! ([View Tweet](https://twitter.com/pikuma/status/1646984466454175744))
	- There we go! Everything connects together. 🙂
	  
	  1. The determinant is interpreted as being the area of the parallelogram between the vectors of our matrix.
	  
	  2. The cross-product magnitude is the area of the parallelogram formed between two vectors A and B.
	  
	  Beautiful stuff! ❤️ ([View Tweet](https://twitter.com/pikuma/status/1646984468111007744))