title:: How Good of a BERT Can O... (highlights)
author:: [[@giffmana on Twitter]]
full-title:: "How Good of a BERT Can O..."
category:: #tweets
url:: https://twitter.com/giffmana/status/1608568387583737856

- Highlights first synced by [[Readwise]] [[Jan 3rd, 2023]]
	- How good of a BERT can one get in ONE DAY on ONE GPU?
	  
	  With all the recent studies about scaling compute up, this paper takes a refreshing turn and does a deep dive into scaling down compute.
	  
	  It's well written, stock full of insights. Here is my summary and my opinions.
	  
	  🧶 1/N 
	  
	  ![](https://pbs.twimg.com/media/FlK1p9lWYAEjcKw.png) ([View Tweet](https://twitter.com/giffmana/status/1608568387583737856))
		- **Note**: Thread
	- 2/N First, the setting. See screenshot for full info, but in short:
	- 3/N implementation is relatively basic. I like that they refrain from jumping to specialized/optimized setups which would be starting in a local minimum right away.
	  
	  Note the odd last paragraph which is greyed out. That's a weird latex mistake to make, isn't it? 
	  
	  ![](https://pbs.twimg.com/media/FlK4JLrXkAMkFPR.jpg) ([View Tweet](https://twitter.com/giffmana/status/1608568393623547905))
	- 4/N Data: en
	- 5a Architecture (sub-thread).
	  
	  Super interesting and echoes our experience in vision: with enough data, all variants reach ~ the same loss in the same wall-clock time. Faster models need to see more tokens. In other words, with good implementations, it's hard to cheat wall-clock. 
	  
	  ![](https://pbs.twimg.com/media/FlK7TKMWAAEkEBs.png) 
	  
	  ![](https://pbs.twimg.com/media/FlK8udhWIAApe2T.png) 
	  
	  ![](https://pbs.twimg.com/media/FlK81NdXEAsVHE7.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FlK85CpXoAA3f3C.jpg) ([View Tweet](https://twitter.com/giffmana/status/1608568399436861440))
	- 5b same thing again: focus model changes to those that keep the same capacity (~params for Transformer MLMs with fixed seqlen) but speed things up.
	  
	  It's a shame that vast majority of papers (including sometimes mine) completely ignore reporting wall-clock speed or slowdowns. 
	  
	  ![](https://pbs.twimg.com/media/FlK9TSKXEAA-sLs.png) ([View Tweet](https://twitter.com/giffmana/status/1608568403190771712))
	- 5c changes include:
	- 6a/N training
	- 6b training: lr schedule!
	  
	  They tried many, but this is where I disagree with the paper.
	  Most schedules either don't warmup (-> lower peak lr!) or don't cooldown (-> 0 at the end).
	  
	  The only two that work clearly better than the rest are the only two with warmup and cooldown! 
	  
	  ![](https://pbs.twimg.com/media/FlLCA62WQAAoi58.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FlLCD16XEAACTTy.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FlLCG_WWQAEjB8h.jpg) ([View Tweet](https://twitter.com/giffmana/status/1608568411855937536))
	- addendum to 6b: the figure from my screenshot is in the appendix. Other papers have shown even pre-norm needs warmup.
	  
	  6c training:
	- 7/N data
	- 8 results
	  
	  left: overall, it's getting pretty close to original BERT which used 45-136x more total FLOPS (4d on 16 TPUs)
	  right: and when training for 16x longer (2d on 8 GPUs), the same recipe actually improves on original BERT quite a bit, reaching RoBERTa levels of performance. 
	  
	  ![](https://pbs.twimg.com/media/FlLG5xcWYAY_cif.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FlLHYw5XwAMp-mu.png) ([View Tweet](https://twitter.com/giffmana/status/1608568420735324161))
	- 9/9 final thoughts.
	- PS: This thread took me almost as long as a paper review. Looks like I procrastinate my CVPR reviews by making twitter paper reviews instead ¯\_(ツ)_/¯ ([View Tweet](https://twitter.com/giffmana/status/1608568425877770240))
	- @albertzeyer ... Trust me it's the same with only dropout, and we ruined the dropout factor and other things too. ([View Tweet](https://twitter.com/giffmana/status/1609600341883998210))