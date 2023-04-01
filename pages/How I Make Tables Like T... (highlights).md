title:: How I Make Tables Like T... (highlights)
author:: [[@buninux on Twitter]]
full-title:: "How I Make Tables Like T..."
category:: #tweets
url:: https://twitter.com/buninux/status/1640280104105390080

- Highlights first synced by [[Readwise]] [[Mar 28th, 2023]]
	- How I make tables like this with Figma. 
	  
	  A quick guide.
	  
	  #uidesign https://t.co/7Ooro8NaDQ ([View Tweet](https://twitter.com/buninux/status/1640280104105390080))
		- **Note**: Thread
	- The table is made of сells, rows, and a header.
	  
	  First, create a variant set to house all variations of your cells and header cell components.
	  
	  Expose nested props to be able to control individual details from the component level. 
	  
	  ![](https://pbs.twimg.com/media/FsNxIWEX0AYOimH.jpg) ([View Tweet](https://twitter.com/buninux/status/1640280106072408064))
	- Combine Header components into an auto layout group. 
	  
	  Customize and add your project information to the header of your table. 
	  
	  ![](https://pbs.twimg.com/media/FsNxcULWYAA4MRA.png) ([View Tweet](https://twitter.com/buninux/status/1640280108018675713))
	- Combine cell components to create a table row. 
	  
	  Customize individual cells using properties to create a row with your project's details.
	  
	  Duplicate the resulting table row to create a full table. 
	  
	  ![](https://pbs.twimg.com/media/FsNxlxFX0AAFuBQ.jpg) ([View Tweet](https://twitter.com/buninux/status/1640280109671219201))
	- Combine header and duplicated table rows into a single Table frame. Set the header and rows to Fill in the width and stay Fixed in height.
	  
	  Note: For all nested cell elements, set the height to Fill. To avoid half pixels on resize. 
	  
	  ![](https://pbs.twimg.com/media/FsNxpy0WYAUc8eb.jpg) ([View Tweet](https://twitter.com/buninux/status/1640280111395090433))
	- Set the cell column you want to hide on resize and set its nested elements width to Fill.
	  
	  Choose the column you want to stay visible on resize and set its nested elements width to stay Fixed. 
	  
	  ![](https://pbs.twimg.com/media/FsNxuq9WcAAT7om.jpg) ([View Tweet](https://twitter.com/buninux/status/1640280114024906752))
	- Shrink it! ✨
	  
	  Control which columns are visible on resize by changing the column width constraints. https://t.co/RvCc8lHHRr ([View Tweet](https://twitter.com/buninux/status/1640280116113596417))
	- Find out more components like this one in the FramesX UI kit.
	  
	  ✓ Variant sets
	  ✓ Auto layout ready
	  ✓ Optimized properties
	  
	  https://t.co/qPAs5ztIew ([View Tweet](https://twitter.com/buninux/status/1640323896216887296))