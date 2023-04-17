title:: K-Means Has Two Major Pr... (highlights)
author:: [[@akshay_pachaar on Twitter]]
full-title:: "K-Means Has Two Major Pr..."
category:: #tweets
url:: https://twitter.com/akshay_pachaar/status/1645048847922794502

- Highlights first synced by [[Readwise]] [[Apr 13th, 2023]]
	- K-Means has two major problems:
		- **Note**: Thread
	- Simply put, DBSCAN groups together points in a dataset that are close to each other based on their spatial density.
	  
	  It's very easy to understand, just follow along ...👇 ([View Tweet](https://twitter.com/akshay_pachaar/status/1645048852146454528))
	- DBSCAN has two important parameters.
	  
	  1️⃣ Epsilon (eps):
	  
	  `eps`:  represents the maximum distance between two points for them to be considered part of the same cluster.
	  
	  Points within this distance of each other are considered to be neighbours.
	  
	  Check this out 👇 
	  
	  ![](https://pbs.twimg.com/media/FtRjN8cakAEbNhv.jpg) ([View Tweet](https://twitter.com/akshay_pachaar/status/1645048861604610048))
	- 2️⃣ min_samples:
	  
	  The minimum number of points that must be present within the eps distance for a point to be considered a core point.
	  
	  Core points are points that have at least min_samples number of neighbours within the eps distance.
	  
	  Check this out 👇 
	  
	  ![](https://pbs.twimg.com/media/FtRjOlKaQAELcWa.jpg) ([View Tweet](https://twitter.com/akshay_pachaar/status/1645048873185058820))
	- Now all the points which are not outliers & within in eps reachability of each, become part of the same cluster.
	  
	  That's it, that's all that DBSCAN is about! 🎉
	  
	  Check this image 👇 
	  
	  ![](https://pbs.twimg.com/media/FtRjPVBacAAgEcK.jpg) ([View Tweet](https://twitter.com/akshay_pachaar/status/1645048894278238208))
	- Now that we understand how DBSCAN works, let's see things in action 🚀
	  
	  Time for some code 🔥
	  
	  First we create some dummy data for clustering!
	  
	  Check this out 👇 
	  
	  ![](https://pbs.twimg.com/media/FtRjQluakAAjQhR.jpg) ([View Tweet](https://twitter.com/akshay_pachaar/status/1645048919188201472))
	- Applying DBSCAN doesn't get easier 🚀
	  
	  Notice that we don't need to worry about number of clusters in the data, it's determined based on density! ✅
	  
	  Check this out 👇 
	  
	  ![](https://pbs.twimg.com/media/FtRjSG0akAIF8VC.jpg) ([View Tweet](https://twitter.com/akshay_pachaar/status/1645048946774114304))
	- 🔵 Find Jupyter Notebook 📒 ⬇️
	  
	  Don't forget to star the repo! 🌟
	  https://t.co/2rvKyKYry9 ([View Tweet](https://twitter.com/akshay_pachaar/status/1645048951828283399))
	- That's a wrap!
	  
	  If you interested in: