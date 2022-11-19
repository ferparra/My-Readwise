title:: /1 How Does 𝐠𝐑𝐏𝐂 Work?... (highlights)
author:: [[@alexxubyte on Twitter]]
full-title:: "/1 How Does 𝐠𝐑𝐏𝐂 Work?..."
category:: #tweets
url:: https://twitter.com/alexxubyte/status/1589661228502171649

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- /1 How does 𝐠𝐑𝐏𝐂 work?
	  
	  RPC (Remote Procedure Call) is called “𝐫𝐞𝐦𝐨𝐭𝐞” because it enables communications between remote services when services are deployed to different servers. From the user’s point of view, it acts like a local function call 
	  
	  ![](https://pbs.twimg.com/media/Fg-cdXRVEAArIQf.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1589661228502171649))
		- **Note**: Thread
	- /2 The diagram below illustrates the overall data flow for 𝐠𝐑𝐏𝐂.
	  
	  Step 1: A REST call is made from the client. The request body is usually in JSON format. 
	  
	  ![](https://pbs.twimg.com/media/Fg-cd6vVUAEVfor.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1589661239747129345))
	- /3 Steps 2 - 4: The order service (gRPC client) receives the REST call, transforms it, and makes an RPC call to the payment service. gPRC encodes the 𝐜𝐥𝐢𝐞𝐧𝐭 𝐬𝐭𝐮𝐛 into a binary format and sends it to the low-level transport layer. 
	  
	  ![](https://pbs.twimg.com/media/Fg-cejeVQAAQssu.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1589661251071713280))
	- /4 Step 5: gRPC sends the packets over the network via HTTP2. Because of binary encoding and network optimizations, gRPC is said to be 5X faster than JSON. 
	  
	  ![](https://pbs.twimg.com/media/Fg-cfNnVIAU9dpX.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1589661261997887489))
	- /5 Steps 6 - 8: The payment service (gRPC server) receives the packets from the network, decodes them, and invokes the server application.
	  
	  Steps 9 - 11: The result is returned from the server application, and gets encoded and sent to the transport layer. 
	  
	  ![](https://pbs.twimg.com/media/Fg-cf2BUUAAroP5.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1589661272915648512))
	- /6 Steps 12 - 14: The order service receives the packets, decodes them, and sends the result to the client application.
	  
	  👉 Over to you: Have you used gPRC in your project? What are some of its limitations? 
	  
	  ![](https://pbs.twimg.com/media/Fg-cge7VUAE9jxb.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1589661283925643264))
	- /7 Subscribe to our weekly newsletter to learn something new every week:
	  https://t.co/dkjDPxrTOt ([View Tweet](https://twitter.com/alexxubyte/status/1589661287801184256))