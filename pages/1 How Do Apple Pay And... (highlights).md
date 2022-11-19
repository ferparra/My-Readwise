title:: /1 How Do Apple Pay And... (highlights)
author:: [[@alexxubyte on Twitter]]
full-title:: "/1 How Do Apple Pay And..."
category:: #tweets
url:: https://twitter.com/alexxubyte/status/1572614943811440642

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- /1 How do Apple Pay and Google Pay handle sensitive card info?
	  
	  The diagram below shows the differences. Both approaches are very secure, but the implementations are different. To understand the difference, we break down the process into two flows. 
	  
	  ![](https://pbs.twimg.com/media/FdMM9CAagAAVnu8.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1572614943811440642))
		- **Note**: Thread
	- /2 1. Registering your credit card flow
	  2. Basic payment flow ([View Tweet](https://twitter.com/alexxubyte/status/1572614947930247168))
	- /3 1️⃣ The registration flow is represented by steps 1~3 for both cases.
	  
	  𝐀𝐩𝐩𝐥𝐞 𝐏𝐚𝐲: It doesn’t store any card info. It passes the card info to the bank. Bank returns a token called DAN (device account number). iPhone then stores DAN into a special hardware chip. 
	  
	  ![](https://pbs.twimg.com/media/FdMM9viaAAM1e2R.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1572614956989960192))
	- /4 𝐆𝐨𝐨𝐠𝐥𝐞 𝐏𝐚𝐲: When you register the credit card with Google Pay, the card info is stored in the Google server. Google returns a payment token to the phone. 
	  
	  ![](https://pbs.twimg.com/media/FdMM-UsaAAMiHxM.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1572614967303741440))
	- /5 2️⃣ When you click the “Pay” button on your phone, the basic payment flow starts. Here are the differences:
	  
	  𝐀𝐩𝐩𝐥𝐞 𝐏𝐚𝐲: For iPhone, the e-commerce server passes the DAN to the bank. 
	  
	  ![](https://pbs.twimg.com/media/FdMM--sacAIzNSb.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1572614978334785541))
	- /6 𝐆𝐨𝐨𝐠𝐥𝐞 𝐏𝐚𝐲: The e-commerce server passes the payment token to the Google server. Google server looks up the card info and passes it to the bank.
	  
	  In the diagram, the red arrow means the credit card info is available on the public network, although it is encrypted. 
	  
	  ![](https://pbs.twimg.com/media/FdMM_jsagAMvU1G.jpg) ([View Tweet](https://twitter.com/alexxubyte/status/1572614988585668610))
	- /7 👉 Over to you: Apple needs to discuss the DAN details with banks. It takes time and effort, but the benefit is that the credit card info is on the public network only once. If you are an architect and have to choose between security and cost, which solution do you prefer? ([View Tweet](https://twitter.com/alexxubyte/status/1572614992507314176))
	- /8 I hope you've found this thread helpful.
	  
	  Follow me @alexxubyte for more.
	  
	  Like/Retweet the first tweet below if you can: https://t.co/MF4sgjyyxV ([View Tweet](https://twitter.com/alexxubyte/status/1572614995279753218))