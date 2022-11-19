title:: Scroll-to-Zoom Is Such A... (highlights)
author:: [[@gilesvangruisen on Twitter]]
full-title:: "Scroll-to-Zoom Is Such A..."
category:: #tweets
url:: https://twitter.com/gilesvangruisen/status/1532770969269374976

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Scroll-to-zoom is such a pervasive interaction, you may think it’s easy to build. You’d be wrong. The first time I built it, I almost lost my mind.
	  
	  The second time, @felt, I learned a few things that made it far more fun to develop. Here’s what I wish I knew the first time 👇 https://t.co/z0H7tB54QY ([View Tweet](https://twitter.com/gilesvangruisen/status/1532770969269374976))
		- **Note**: Thread
	- @felt Scrolling with a mouse wheel or trackpad is one of the most natural gestures on a computer, but how it works depends largely on context…
	  
	  Interactive canvases like Figma, Google Earth, or Photoshop use one of two primary scrolling modes: pan or zoom. ([View Tweet](https://twitter.com/gilesvangruisen/status/1532770972951928832))
	- @felt Most of us are pretty familiar with maps like Apple and Google, which let you scroll to zoom the map in and out. Design tools like Figma, on the other hand, treat scrolling gestures as a pan by default (like scrolling a webpage): https://t.co/uMN7loCYHw ([View Tweet](https://twitter.com/gilesvangruisen/status/1532770985509695488))
	- @felt We ran into this question early on at @Felt, and landed on scroll-to-zoom.
	  
	  Mapping experts come from more of a design tool background, but to turn everyone into a map maker our tool needs to feel as familiar as the mapping tools they're already used to. ([View Tweet](https://twitter.com/gilesvangruisen/status/1532770988445736962))
	- @felt Making this zooming behavior actually work is a bit trickier. The user's map position at any given moment is determined by a zoom level and the lat/lng at the center of the screen. 
	  
	  Unfortunately, it's not enough to simply increase and decrease the zoom level: https://t.co/xWnMfvqTmh ([View Tweet](https://twitter.com/gilesvangruisen/status/1532771019512877059))
	- @felt Most of the time you want to zoom in *on a place*, wherever you're pointing the mouse, so we also need to pan the map by the correct amount to ensure that place stays underneath your cursor.
	  
	  But how do we calculate how much to move the map? ([View Tweet](https://twitter.com/gilesvangruisen/status/1532771024160186368))
	- @felt Ultimately, we need to figure out the new center point of the map, so we first measure the offset from the map's center to the cursor in pixels; the center coordinate at the new zoom level should be the same pixel distance from the cursor as the old center. 
	  
	  ![](https://pbs.twimg.com/media/FUV_IPDVsAIbsLv.jpg) ([View Tweet](https://twitter.com/gilesvangruisen/status/1532771033001824256))
	- @felt Next, we can project the cursor position into geographic space, and calculate our cursor offset in degrees, based on the new zoom level.
	  
	  Our new center coordinate is the result of adding that degree offset to the cursor's geographic coordinate: https://t.co/KPeWIjITku ([View Tweet](https://twitter.com/gilesvangruisen/status/1532771058448670720))
	- @felt It's easy to forget how much hidden complexity resides in the interaction patterns we use every day.
	  
	  Especially with any kind of mapping or canvas tool, there are so many behaviors users might take for granted, but they're pretty fun to build! 😄
	  
	  https://t.co/dfFSJfItkp ([View Tweet](https://twitter.com/gilesvangruisen/status/1532771062185725952))
	- @felt Oh yeah, we're hiring! If this sounds fun to you, check out https://t.co/QozvbuSgvv ([View Tweet](https://twitter.com/gilesvangruisen/status/1532771064811429889))