title:: AI Like GPT-3 and Others... (highlights)
author:: [[@abacaj on Twitter]]
full-title:: "AI Like GPT-3 and Others..."
category:: #tweets
url:: https://twitter.com/abacaj/status/1608163940726358024

- Highlights first synced by [[Readwise]] [[Dec 30th, 2022]]
	- AI like GPT-3 and others have come a long way, we can now build complex use cases with state of the art AI models
	  
	  Here's a quick thread on how I built a prototype for book whisperer, which let's you talk to an AI (GPT-3) and ask questions on a particular book 👇
	  
	  1/10 
	  
	  ![](https://pbs.twimg.com/media/FlFVA7XX0AEKPrm.jpg) ([View Tweet](https://twitter.com/abacaj/status/1608163940726358024))
		- **Note**: Thread
	- First thing we need to do is process the book, in my prototype it means we take a PDF of the book "Intro to Algorithms" and turn the pages into images
	  
	  We do this by using a image processing library called ImageMagick: https://t.co/IENLLKbr8p
	  
	  2/10 ([View Tweet](https://twitter.com/abacaj/status/1608163943234633728))
	- Example command with ImageMagick:
	  convert -density 150 -trim -background white -alpha remove /imgs/introalgo.pdf[45] -quality 100 flatten -sharpen 0x1.0 /imgs/p45.png
	  
	  This takes a page from the PDF (p.45) and outputs a nicely formatted image, we do this for every page
	  
	  3/10 
	  
	  ![](https://pbs.twimg.com/media/FlFPgU7WQAEe03y.jpg) ([View Tweet](https://twitter.com/abacaj/status/1608163945201680387))
	- With the images in hand we now need to get text output for book whisperer. To do this we use a OCR engine called Tesseract: https://t.co/bhLvpkhbTz
	  
	  Example command with tess:
	  tesseract p45.png p45 --oem 1 -l eng
	  
	  We now have a pretty good textual representation of page 45
	  
	  4/10 
	  
	  ![](https://pbs.twimg.com/media/FlFQUn1XwAEaUva.jpg) ([View Tweet](https://twitter.com/abacaj/status/1608163947248758784))
	- The text by itself is already useful, but the book is large, over 1200 pages!
	  
	  This now turns into a search problem. When we ask a question about the book, we need to reduce the search space that relates to the question
	  
	  5/10 
	  
	  ![](https://pbs.twimg.com/media/FlFUrqJX0AME8xP.png) ([View Tweet](https://twitter.com/abacaj/status/1608163950402707460))
	- To solve for this we make use of OpenAI's text embedding model to convert the text (each page of text) into a vector
	  
	  The text can now be used for search retrieval, read more here on how to do this: https://t.co/yYjMzzbX9Y
	  
	  6/10 
	  
	  ![](https://pbs.twimg.com/media/FlFSSuLWAAIlTvq.png) ([View Tweet](https://twitter.com/abacaj/status/1608163952025821185))
	- We now compute the distance or similarity of the question to the page vectors using a cosine or dot product function (0 to 1 score)
	  
	  This reduces the search space to the top matching pages, we can further limit the results down by taking the top 10 pages~
	  
	  7/10 ([View Tweet](https://twitter.com/abacaj/status/1608163954173554688))
	- Now that we have (1-10) pages in hand, it's time to see how we can use GPT-3 to further help refine the large problem space
	  
	  Given the original question:
	  "What is the running time of an algorithm?"
	  
	  We need GPT-3 to summarize each page to solve for too many tokens
	  
	  8/10 ([View Tweet](https://twitter.com/abacaj/status/1608163955599351808))
	- You can see below the GPT-3 prompt used for each of the 10~ pages
	  
	  This reduces the output tokens for each page to something that will fit into a single prompt later
	  
	  9/10 
	  
	  ![](https://pbs.twimg.com/media/FlFWq0aX0AUsJCD.jpg) ([View Tweet](https://twitter.com/abacaj/status/1608163957302231041))
	- The final GPT-3 prompt with all summaries can be seen in the screenshot along with the output
	  
	  Now, we have a sufficiently advanced "book whisperer" that can answer many, many questions related to the book "Intro to Algorithms" 📕
	  
	  Idea was inspired by @tszzl 
	  
	  10/10 
	  
	  ![](https://pbs.twimg.com/media/FlFXzf4WQAAoFJA.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FlFYOHrWAAAc8UU.png) ([View Tweet](https://twitter.com/abacaj/status/1608163959009337347))