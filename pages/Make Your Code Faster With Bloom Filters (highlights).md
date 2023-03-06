title:: Make Your Code Faster With Bloom Filters (highlights)
author:: [[Miško Hevery (Builder.io/Qwik)]]
full-title:: "Make Your Code Faster With Bloom Filters"
category:: #articles
url:: https://twitter.com/mhevery/status/1628249257462607872
document_note:: Bloom filters are data structures that are like HashMaps but smaller and allow for more efficient operations. They can be used to answer if a key is NOT present with 100% certainty and save from having to do expensive search operations. They work by converting a key with a hash() function into a number and using that number to set a bit in a bit-array. To further improve false positives, multiple hash() functions and larger bit-arrays can be used.
tags:: #[[computer science]] #[[data structures]]

- Highlights first synced by [[Readwise]] [[Feb 25th, 2023]]
	- Bloom filters use a hash() to convert KEY -> number.
	  
	  The number is then modulo bit array size and used to set a bit in bit-array. ([View Highlight](https://read.readwise.io/read/01gsx3wanratxvx5v2r6amkvws))
	- ![](https://pbs.twimg.com/media/Fpi0GR8acAAakSM.jpg) ([View Highlight](https://read.readwise.io/read/01gsx3x6g5b8genpw5xdywpv62))