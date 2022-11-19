title:: (1/21) Cryptography Fund... (highlights)
author:: [[@SalomonCrypto on Twitter]]
full-title:: "(1/21) Cryptography Fund..."
category:: #tweets
url:: https://twitter.com/SalomonCrypto/status/1580388773937881093

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- (1/21) Cryptography Fundamentals: Diffie-Hellman Key Exchange
	  
	  How do you share private information over public networks? How can we create mathematically secure secrets? What actually is an encryption key?
	  
	  A public guide for private communication. 
	  
	  ![](https://pbs.twimg.com/media/Fe6rNncUcAEqLIt.jpg) ([View Tweet](https://twitter.com/SalomonCrypto/status/1580388773937881093))
		- **Note**: Thread
	- (2/21) Let's say you need to communicate sensitive data across a public channel. If you know other people can read your data, you might decide to cryptographically encode it.
	  
	  Encoding is the process of transforming the original data into an undecipherable (but reversible) form. ([View Tweet](https://twitter.com/SalomonCrypto/status/1580388777381412864))
	- (3/21) Encoding is only useful in one condition: if (ONLY) the intended recipient can decode the message, transforming it back into its original form.
	  
	  If we can pull this off, we can securely share sensitive data even while broadcasting it to the entire world. ([View Tweet](https://twitter.com/SalomonCrypto/status/1580388780011159553))
	- (4/21) In order to do this, we use a cryptographic algorithm. A cryptographic algorithm receives a message and an encryption key.
	  
	  If the message is not encrypted, the algorithm will encode it.
	  
	  If the message is encrypted, the algorithm will decode it. ([View Tweet](https://twitter.com/SalomonCrypto/status/1580388782787817472))
	- (5/21) We will just take the cryptographic algorithm for granted; you can just treat it like a black box. We are interested in the encryption key.
	  
	  More specifically, we are interested in understanding how to create a key. ([View Tweet](https://twitter.com/SalomonCrypto/status/1580388785602252800))
	- (6/21) Due to the nature of a cryptographic algorithm, anyone with the encryption key is able to decode the message.
	  
	  If you don't have a private channel to create/agree upon the key, how can do it in the open?
	  
	  How do you establish a shared secret in public? ([View Tweet](https://twitter.com/SalomonCrypto/status/1580388788169150464))
	- (7/21) Our answer comes from over 40 years ago by Whitfield Diffie and Martin Hellman: Diffie-Hellman Key Exchange.
	  
	  This scheme was the first method of creating a shared secret that didn't require the literal physical exchange of encryption keys (via paper, disk, etc). ([View Tweet](https://twitter.com/SalomonCrypto/status/1580388790773817344))
	- (8/21) Before we get started, we need to cover some basic math (don't worry, it's not bad)
	  
	  When you divide two integers, sometimes the result is not an integer (eg has a reminder). Modular arithmetic is a branch of math that is focused on the reminder
	  
	  https://t.co/W9X1Rs6Jsn ([View Tweet](https://twitter.com/SalomonCrypto/status/1580388793361715200))
	- (9/21) The modulo operator (written as "mod") is the operation that finds the remainder.
	  
	  10 / 3 = 3 with a remainder of 1 = 10 mod 3 = 1
	  14 / 6 = 2 with a remainder of 2 = 14 mod 6 = 2
	  3 / 10 = 0 with a remainder of 3 = 3 mod 10 = 3
	  
	  Imagine a clock being mod 12. ([View Tweet](https://twitter.com/SalomonCrypto/status/1580388795974705152))
	- (10/21) Ok, that's it! All the math you need.
	  
	  Is that too much? No worries! Diffie-Hellman has a classic metaphor that is very helpful: mixing paint. In the metaphor, the goal is to create a secret color that only the participants know. ([View Tweet](https://twitter.com/SalomonCrypto/status/1580388798617202689))
	- (11/21) Diffie-Hellman begins with two parties (Satoshi, Vitalik), a public data channel and two publicly available numbers: g and n (yellow).
	  
	  g and n are either agreed upon before hand, using some industry standard, or are agreed upon in public before the process starts. 
	  
	  ![](https://pbs.twimg.com/media/Fe6rPgYVQAAycTM.jpg) ([View Tweet](https://twitter.com/SalomonCrypto/status/1580388808196882432))
	- (12/21) Both parties have a secret number (Satoshi - a, red) (Vitalik - b, blue). These numbers are the keys to every message sent by their owner; their privacy is paramount. ([View Tweet](https://twitter.com/SalomonCrypto/status/1580388811455967232))
	- (13/21) To begin the process, both parties import the publicly available data (g and n - yellow) and apply their secret number.
	  
	  The formula below is a little scary; let me break it down.
	  
	  All we are doing is multiplying g by itself a/b times and then applying mod n. 
	  
	  ![](https://pbs.twimg.com/media/Fe6rQJaVUAEDlMa.jpg) ([View Tweet](https://twitter.com/SalomonCrypto/status/1580388819135696896))
	- (14/21) Here is a concrete example: 
	  
	  ![](https://pbs.twimg.com/media/Fe6rQnKUYAARQUO.png) 
	  
	  ![](https://pbs.twimg.com/media/Fe6rQzJUYAMJm5A.png) ([View Tweet](https://twitter.com/SalomonCrypto/status/1580388828623167489))
	- (15/21) Next, both parties will send this new value back across the public channel.
	  
	  At this point both values become public, however no observer can recover the original data. The critical piece is the modulo function. 
	  
	  ![](https://pbs.twimg.com/media/Fe6rRJeUAAMcV8J.jpg) ([View Tweet](https://twitter.com/SalomonCrypto/status/1580388836936273920))
	- (16/21) Let's think about a clock as a system with mod 12.
	  
	  Just because you know we start at 4 (g) and where we end at 6 (g^a mod n) doesn't give you enough information to know how long we lasted: 2 hours? 14 hours? 26 hours?
	  
	  g^a mod n is the same problem! ([View Tweet](https://twitter.com/SalomonCrypto/status/1580388840346304514))
	- (17/21) It turns out there isn't a great way to do this other to just start guessing. Our examples are using tiny numbers, but in practice these values would be hundreds of digits long.
	  
	  Guessing is not just difficult, its nearly impossible (although that's becoming less true). ([View Tweet](https://twitter.com/SalomonCrypto/status/1580388842992898048))
	- (18/21) Once both parties have this intermediate value, they can repeat the process they used to make it: multiply the new value a/b times and take the remainder when you divide by n.
	  
	  Here's where the magic happens: Now you both have the same number; a number no one else knows. ([View Tweet](https://twitter.com/SalomonCrypto/status/1580388845639475200))
	- (19/21) Here is a concrete example: 
	  
	  ![](https://pbs.twimg.com/media/Fe6rSHmVIAEFONX.png) 
	  
	  ![](https://pbs.twimg.com/media/Fe6rSTHUoAA9649.png) ([View Tweet](https://twitter.com/SalomonCrypto/status/1580388854405599232))
	- (20/21) And so, after you complete the Diffie-Hellman key exchange process, both parties have a shared secret. They both can be confident that they (and only they) will the only ones able to read messages that use that value as an encryption key.
	  
	  A public secret! ([View Tweet](https://twitter.com/SalomonCrypto/status/1580388857186439170))
	- (21/21) Audio/video learner? No problem! @computer_phile has got you covered!
	  
	  Classic paint metaphor:
	  https://t.co/0GqwUp2e2l
	  
	  Actual math:
	  https://t.co/1LoyhlZqGI ([View Tweet](https://twitter.com/SalomonCrypto/status/1580388859807879168))
	- Like what you read? Help me spread the word by retweeting the thread (linked below).  
	  
	  Follow me for more explainers and as much alpha as I can possibly serve. https://t.co/ANXKnfOirk ([View Tweet](https://twitter.com/SalomonCrypto/status/1580390420814577664))