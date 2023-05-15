title:: 1/ This Week We Released... (highlights)
author:: [[@TimDarcet on Twitter]]
full-title:: "1/ This Week We Released..."
category:: #tweets
url:: https://twitter.com/TimDarcet/status/1649435730291093506

- Highlights first synced by [[Readwise]] [[Apr 22nd, 2023]]
	- 1/ This week we released DINOv2: a series of general vision encoders pretrained without supervision. Good out-of-the-box performance on a variety of domains, matching or surpassing other publicly available encoders. https://t.co/3onXIH0fOt ([View Tweet](https://twitter.com/TimDarcet/status/1649435730291093506))
		- **Note**: Thread
	- 2/ As opposed to other recent SSL works, the goal is to provide vision encoders that work off-the-shelf, without any fine-tuning. In this setup, we improve significantly over previous SSL works, and even match or surpass CLIP-type models on a variety of tasks 
	  
	  ![](https://pbs.twimg.com/media/FuP2pjuXgAI5AfC.jpg) ([View Tweet](https://twitter.com/TimDarcet/status/1649435733902475266))
	- 3/ TL;DR of results (on the benchmarks we tested) is
	  Classification: DINOv2 ≥ CLIP
	  Dense tasks (segmentation, depth): DINOv2 > CLIP
	  Retrieval: DINOv2 > CLIP ([View Tweet](https://twitter.com/TimDarcet/status/1649435736641269760))
	- 4/ For dense tasks, it makes sense: captions only capture image information up to a certain point, they miss local information. The masked image modeling loss in DINOv2 (from iBOT) gives it local understanding. 
	  
	  ![](https://pbs.twimg.com/media/FuP21qcWAAEj1HC.jpg) ([View Tweet](https://twitter.com/TimDarcet/status/1649435738327375872))
	- 5/  The good knn properties of DINO and the new KoLeo regularization combine to produce strong retrieval results. We were surprised by how good the metrics are! Even our ViT-S reaches better scores than any previously released model. 
	  
	  ![](https://pbs.twimg.com/media/FuP3DmIXsAEXm94.jpg) ([View Tweet](https://twitter.com/TimDarcet/status/1649435741435338753))
	- 6/ With these capabilities emerge new interesting properties. A very nice one is the ability to perform semantic keypoint matching between images simply by matching the closest features. This works across very different domains ! 
	  
	  ![](https://pbs.twimg.com/media/FuP3Vc2XsAExXFP.png) 
	  
	  ![](https://pbs.twimg.com/media/FuP3YrpWwAUqtiu.png) 
	  
	  ![](https://pbs.twimg.com/media/FuP3cMEWIAExDG0.png) ([View Tweet](https://twitter.com/TimDarcet/status/1649435744023330817))
	- 7/ What's the secret ingredient then? Well, the simplest answers are often the best. Most improvements come from scaling up, tuning carefully, stabilizing the training, efficient implementations... Might seem scientifically boring, but it’s absolutely crucial. ([View Tweet](https://twitter.com/TimDarcet/status/1649435747672289285))
	- 8/ A few changes:
	- 9/ There's a bit to be said about the dataset too: we automatically curate 1B image to 140M with a retrieval+deduplication pipeline. More diverse than Imagenet22k, while still having better image quality and balance than uncurated datasets (YFCC, LAION, IG2B...) 
	  
	  ![](https://pbs.twimg.com/media/FuP4ck0XsAYPrqF.jpg) ([View Tweet](https://twitter.com/TimDarcet/status/1649435753825312768))
	- 10/ We used a big model: 1B params. We needed a memory-efficient attention (upstreamed to pytorch2!), a better stochastic depth implem, and a few other optimisations... Our code is 2x faster and is 3x less memory than the DINO/iBOT repos. All code usable in our repo ! ([View Tweet](https://twitter.com/TimDarcet/status/1649435756752928772))
	- 11/ But giant models are impractical. To create smaller, portable models, we distilled the ViT-g into ViT-S, B and L (50x, 14x and 3x smaller). Distilling improves significantly over training from scratch! At these sizes, our distilled models beat all other models we tested. 
	  
	  ![](https://pbs.twimg.com/media/FuP453SWYAEAQbW.jpg) ([View Tweet](https://twitter.com/TimDarcet/status/1649435758380425217))
	- 12/ Also check out the demo! Segmentation, depth and retrieval, easily accessible.
	  Arxiv: https://t.co/dsP3KtICm7
	  Demo: https://t.co/a02p1wEU40
	  Github: https://t.co/fGU8hmynNF ([View Tweet](https://twitter.com/TimDarcet/status/1649470193880399872))