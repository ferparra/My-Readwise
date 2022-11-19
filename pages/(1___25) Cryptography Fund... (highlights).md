title:: (1/25) Cryptography Fund... (highlights)
author:: [[@SalomonCrypto on Twitter]]
full-title:: "(1/25) Cryptography Fund..."
category:: #tweets
url:: https://twitter.com/SalomonCrypto/status/1580677281474699264

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- (1/25) Cryptography Fundamentals: Elliptic Curve Cryptography
	  
	  Elliptic Curve Cryptography is (one of) our strongest cryptographic tools, vastly more secure than its predecessors. But... how does the moon math at the center of modern crypto work?
	  
	  A layman's guide to Sci-Fi tech 
	  
	  ![](https://pbs.twimg.com/media/Fe-xmLbUUAARO3X.jpg) 
	  
	  ![](https://pbs.twimg.com/media/Fe-xmc7UcAAsR9H.jpg) 
	  
	  ![](https://pbs.twimg.com/media/Fe-xmunUYAEEB13.jpg) 
	  
	  ![](https://pbs.twimg.com/media/Fe-xnAKUcAAyLIj.png) ([View Tweet](https://twitter.com/SalomonCrypto/status/1580677281474699264))
		- **Note**: Thread
	- (2/25) The internet is a very public place. It basically works by blasting information at anyone listening, hoping it’ll get to its intended recipient.
	  
	  Need to send a private message? Someone else WILL get a copy of the data; you’re going to need a cryptographic algorithm. ([View Tweet](https://twitter.com/SalomonCrypto/status/1580677285102788608))
	- (3/25) A cryptographic algorithm receives a message and an encryption key.
	  
	  If the message is not encrypted, the algorithm will transform it into illegible nonsense, securing the data.
	  
	  If the message is encrypted (and the key matches the encoding), the algorithm will decode it. ([View Tweet](https://twitter.com/SalomonCrypto/status/1580677287757824001))
	- (4/25) Just treat encryption algorithms like a black box, let’s focus on the encryption keys.
	  
	  Anyone that has a copy has access to your messages, so we need to ensure it stays secret between you and whoever you’re talking to.
	  
	  So… how do we create a shared secret in public? ([View Tweet](https://twitter.com/SalomonCrypto/status/1580677290446376960))
	- (5/25) The first answer is Diffie-Hellman Key Exchange, a process that allows two entities to privately generate a shared secret by sharing public information.
	  
	  (From here on there’s math, but it’s easy. You do need to know modular arithmetic, covered in the linked thread). https://t.co/ANXKnfOirk ([View Tweet](https://twitter.com/SalomonCrypto/status/1580677293118136321))
	- (6/25) The crux of Diffie-Hellman is in the equation below - specifically in how incredibly difficult it is to undo.
	  
	  The problem with modular arithmetic is it’s very difficult to figure out how many times the value looped through the maximum. 
	  
	  ![](https://pbs.twimg.com/media/Fe-xn_pUYAEz5Q9.jpg) ([View Tweet](https://twitter.com/SalomonCrypto/status/1580677299225079809))
	- (7/25) Let’s say you are listening to a Diffie-Hellman exchange. You are able to learn:
	  
	  n = 23
	  g = 5
	  g^a mod n = 4
	  
	  We know g^a has a remainder of 4… that’s not enough info. Does g^a = 27? 50? 73? There are literally infinite options. https://t.co/1B92kqYyGe ([View Tweet](https://twitter.com/SalomonCrypto/status/1580677302391742464))
	- (8/25) One way to do it is to just start guessing. Quickly you’ll realize that a = 4. But with sufficiently large numbers, this can take forever.
	  
	  Computation in one direction is easy, but undoing it is super difficult. We call these types of functions Trapdoor Functions. ([View Tweet](https://twitter.com/SalomonCrypto/status/1580677305189339137))
	- (9/25) Trapdoor functions form the basis of strong encryption.
	  
	  First Diffie-Hellman built a protocol around modular arithmetic.
	  
	  Next, RSA extended on these ideas to build around factoring large numbers.
	  
	  Unfortunately, we are starting to get better and better at solving both. ([View Tweet](https://twitter.com/SalomonCrypto/status/1580677307852693505))
	- (10/25) In summary, this is the world we find ourselves in:
	  
	  1) cryptography is about creating shared secrets using public channels
	  2) a trapdoor function provides the foundation for cryptographic security
	  3) we are getting to good at solving the old trapdoor functions ([View Tweet](https://twitter.com/SalomonCrypto/status/1580677310402813952))
	- (11/25) This is where elliptic curve cryptography comes into play. The elliptic curve provides the context needed for a (much) better trapdoor function.
	  
	  We begin with an elliptic curve, defined below. 
	  
	  ![](https://pbs.twimg.com/media/Fe-xo__VsAA26AY.jpg) ([View Tweet](https://twitter.com/SalomonCrypto/status/1580677316962750464))
	- (12/25) We will define the dot operation to take advantage of the curve’s unique shape and horizontal symmetry.
	  
	  Shape: a line drawn through 2 points will intersect with the curve once (and only once) more
	  
	  Symmetry: the curve always exists in the same place opposite the x-axis. 
	  
	  ![](https://pbs.twimg.com/media/Fe-xpZCUcAAEGm8.jpg) ([View Tweet](https://twitter.com/SalomonCrypto/status/1580677324608937985))
	- (13/25) If you’re paying close enough attention, you can already see the trapdoor function begin to form
	  
	  Need a hint? Modular arithmetic was difficult to undo because you can’t tell how many times the value looped over the maximum (n). 1 iteration is indistinguishable from 1000 ([View Tweet](https://twitter.com/SalomonCrypto/status/1580677327863705601))
	- (14/25) This is what we are going to build out of the dot operation, but first we need to prepare our workspace.
	  
	  In its current state, an elliptic curve is much to infinite. How many values exist between x = 1 and x = 2? How big can the values get? ([View Tweet](https://twitter.com/SalomonCrypto/status/1580677330459979777))
	- (15/25) We are going to apply two operations to our curve:
	- (16/25) The discrete field still retains the properties required to implement the dot operation.
	  
	  Most importantly, the field retains horizontal symmetry (symmetry across the x-axis). Take a look: 
	  
	  ![](https://pbs.twimg.com/media/Fe-xqoeVQAA7CnF.png) ([View Tweet](https://twitter.com/SalomonCrypto/status/1580677344431259649))
	- (17/25) In fact, dot operations in these finite fields are nearly identical to dot operations in elliptical curves
	  
	  Each dot operation creates a line between two points, continuing until it intersects one more point. Then just flip across the x-axis and find the symmetrical point 
	  
	  ![](https://pbs.twimg.com/media/Fe-xq-2VUAA7BK5.png) ([View Tweet](https://twitter.com/SalomonCrypto/status/1580677351666372608))
	- (18/25) During the dot operation, if our line moves outside the bounds we've set, we simply wrap the line around.
	  
	  Did you ever play the game Asteroids? Same idea: if you move off the screen you just reappear on the other side with the same trajectory. https://t.co/sapAzbwqlt ([View Tweet](https://twitter.com/SalomonCrypto/status/1580677363326586880))
	- (19/25) Computing the number of times a point was dotted is a process called the elliptic curve discrete logarithm function; turns out that the function is INCREDIBLY hard to solve.
	  
	  In fact, there isn't a better method than just guessing and checking. ([View Tweet](https://twitter.com/SalomonCrypto/status/1580677366547853312))
	- (20/25) Just like a Diffie-Hellman system, we can build a system based on the elliptic curve that uses this one-way function to create a shared secret.
	  
	  Diffie-Hellman uses a prime maximum (n), a base public base (g) and a private key (a or b) to generate a shared secret. ([View Tweet](https://twitter.com/SalomonCrypto/status/1580677369190195202))
	- (21/25) An elliptic curve system is (can be) defined by picking a prime number as a max, a curve equation and a public point on the curve.
	  
	  A private key is a number PRIV, and a public key is the public point dotted with itself PRIV times. ([View Tweet](https://twitter.com/SalomonCrypto/status/1580677371769733121))
	- (22/25) When comparing elliptic curve and Diffie-Hellman (and RSA) cryptography, we must compare trapdoor functions.
	  
	  We've made progress on factoring, improving our solving process and increasing computing power. Diffie-Hellman (and RSA) are becoming less and less secure. ([View Tweet](https://twitter.com/SalomonCrypto/status/1580677374395359233))
	- (23/25) Elliptic curve discrete logarithm function? It's been ~30 years and STILL no one has anything better than guessing.
	  
	  The result: for numbers of the same size, solving elliptic curve discrete logarithms is significantly harder than factoring. ([View Tweet](https://twitter.com/SalomonCrypto/status/1580677376995835904))
	- (24/25) Arjen Lenstra framed it best in Universal Security
	  
	  Tl;dr breaking a 228-bit RSA key requires less energy to than it takes to boil a teaspoon of water. Breaking a 228-bit elliptic curve key requires enough energy to boil all the water on earth.
	  
	  https://t.co/KCmosFDBSG 
	  
	  ![](https://pbs.twimg.com/media/Fe-xs27UcAA4HtN.png) ([View Tweet](https://twitter.com/SalomonCrypto/status/1580677382947495936))
	- (25/25) Cryptography is the quest to transfer private data through public channels. Alas, we live in a human world; humans inevitably try to break into secrets
	  
	  First, Diffie and Hellman (& Merkle) gave us a tool; one that's aging (quickly)
	  
	  Fortunately, we have elliptic curves! ([View Tweet](https://twitter.com/SalomonCrypto/status/1580677385912868865))
	- Like what you read? Help me spread the word by retweeting the thread (linked below).  
	  
	  Follow me for more explainers and as much alpha as I can possibly serve. 
	  
	  https://t.co/UvNuVcEwt7 ([View Tweet](https://twitter.com/SalomonCrypto/status/1580677641426075649))