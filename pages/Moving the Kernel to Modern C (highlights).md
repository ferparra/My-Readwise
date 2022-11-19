title:: Moving the Kernel to Modern C (highlights)
author:: [[lwn.net]]
full-title:: "Moving the Kernel to Modern C"
category:: #articles
url:: https://lwn.net/SubscriberLink/885941/01fdc39df2ecc25f/

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Koschel included a
	  patch fixing a bug in the USB subsystem where the iterator passed to
	  this macro was used 
	  after the exit from the macro, which is a dangerous thing to do.  Depending
	  on what happens within the list, the contents of that iterator could be
	  something surprising, even in the absence of speculative execution.
	  Koschel fixed the problem by reworking the code in question to stop using
	  the iterator after the loop.