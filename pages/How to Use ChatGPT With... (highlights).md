title:: How to Use ChatGPT With... (highlights)
author:: [[@Claybight on Twitter]]
full-title:: "How to Use ChatGPT With..."
category:: #tweets
url:: https://twitter.com/Claybight/status/1624457799798497280

- Highlights first synced by [[Readwise]] [[Feb 12th, 2023]]
	- How to use ChatGPT with Excel and SQL tables: ([View Tweet](https://twitter.com/Claybight/status/1624457799798497280))
		- **Note**: Thread
	- What you will learn in this thread:
	  
	  1. How to work with tables in ChatGPT or in https://t.co/mjwrlZ23KR
	  2. How to change these tables with AI.
	  3. How to generate Excel formulas.
	  4. How to create an SQL data model readable by AI.
	  5. How to generate SQL queries. ([View Tweet](https://twitter.com/Claybight/status/1624457802369597442))
	- ChatGPT is down at the moment, and does not print out tables.
	  
	  So I resorted to using my own ChatGPT clone for this thread.
	  
	  Let's get some data from Wikipedia. Copy the top 10 rows.
	  https://t.co/hFrt2RKMpn 
	  
	  ![](https://pbs.twimg.com/media/Fos7xLOaYAE2yZD.jpg) ([View Tweet](https://twitter.com/Claybight/status/1624457814088491011))
	- We need to convert the table to a ChatGPT friendly format.
	  
	  We do this using https://t.co/amtxfrNFun
	  
	  Remember to use compact mode, and delete the column with the description, as each character counts.
	  
	  Copy the generated text. 
	  
	  ![](https://pbs.twimg.com/media/Fos7x2AaIAAHUcG.jpg) ([View Tweet](https://twitter.com/Claybight/status/1624457826503639041))
	- Now paste it into ChatGPT or in this case https://t.co/9bRCZ6ScGV (chat coming next week)
	  
	  It should look like this.
	  
	  As the table is formatted as markdown Aloy can read this and convert it. 
	  
	  ![](https://pbs.twimg.com/media/Fos7yhiaUAAa1fg.jpg) ([View Tweet](https://twitter.com/Claybight/status/1624457838579048448))
	- Aloy reads and understands what the table is about. Now we can ask questions to the table.
	  
	  Let's say we want to add more data. I want a column with the continent.
	  
	  Lets try asking it to add the column Continent. 
	  
	  ![](https://pbs.twimg.com/media/Fos7zNQaQAAQEla.jpg) ([View Tweet](https://twitter.com/Claybight/status/1624457848171401218))
	- We ask it to add the column continent.
	  
	  Aloy has to infer what we mean. It first reasons out which continent the countries are located.
	  
	  Southeast Asia is incorrectly added as a continent. The model is probably influenced by USA in NORTH America, then Indonesia in SOUTHeast Asia. 
	  
	  ![](https://pbs.twimg.com/media/Fos7zwPaYAAoU9A.jpg) ([View Tweet](https://twitter.com/Claybight/status/1624457857856061440))
	- This is not as bad as when Google got its share price cut down due to its new ChatGPT clone Bard making a similar mistake.
	  
	  Remember that language models are probabilistic.
	  
	  You need to be aware of this when using its outputs. 
	  
	  ![](https://pbs.twimg.com/media/Fos70S0acAEVMYC.jpg) ([View Tweet](https://twitter.com/Claybight/status/1624457868123709440))
	- Let's add a column with a formula.
	  
	  We want to add the population percentage of the total.
	  
	  Does Aloy understand how to calculate this using the data in the table?
	  
	  Let's ask: 
	  
	  ![](https://pbs.twimg.com/media/Fos708GaEAAozCN.jpg) ([View Tweet](https://twitter.com/Claybight/status/1624457879809048576))
	- It understood that the total was located in the table, thinking population column was the A column. In this case A1 is total, while A2 is the population in China.
	  
	  It then found the correct formula =A2/A1.
	  
	  But why is Population the A column?
	  
	  We can ask it to query with SQL: 
	  
	  ![](https://pbs.twimg.com/media/Fos71o-acAE3XWF.jpg) ([View Tweet](https://twitter.com/Claybight/status/1624457890420658177))
	- We didn't specify the data model, so it invented its own.
	  
	  We could specify the data model and see if it can correctly query a data model.
	  
	  Let's specify a model.
	  
	  Create a new table, with the list of tables, primary keys and columns. 
	  
	  ![](https://pbs.twimg.com/media/Fos72NzaUAE-QH_.jpg) ([View Tweet](https://twitter.com/Claybight/status/1624457900994465792))
	- Let's then ask for the total population in each continent.
	  
	  Aloy would need to join the tables and group by correctly.
	  
	  Do you see the mistake? 
	  
	  ![](https://pbs.twimg.com/media/Fos721WaQAIjdk2.jpg) ([View Tweet](https://twitter.com/Claybight/status/1624457910637166592))
	- Aloy didn't understand that the column year is the year of the population count.
	  
	  We can just ask it to only do it for 2022. 
	  
	  ![](https://pbs.twimg.com/media/Fos73Z4akAAG9vQ.jpg) ([View Tweet](https://twitter.com/Claybight/status/1624457920061788160))
	- Now you should know how to do this with any table you might have in Excel or a Database.
	  
	  Want more?
	  
	  Check out this thread on the prompt used by the Bing ChatGPT bot codenamed "Sydney"!: https://t.co/u0DbLnTJ7Q ([View Tweet](https://twitter.com/Claybight/status/1624457924352552960))
	- Also, consider following me @Claybight
	  
	  And subscribe to my newsletter about using AI, language models, and prompting to create value:
	  https://t.co/uc9lwIFwBq ([View Tweet](https://twitter.com/Claybight/status/1624457927133376512))
	- TL;DR
	  
	  How to use tabular data in ChatGPT
	  
	  1. Get the data from a table
	  2. Convert it to Markdown readable format
	  3. Paste it into ChatGPT
	  4. Ask questions about the data
	  5. Generate excel formulas
	  6. Define a table schema
	  7. Get ChatGPT to generate SQL statements ([View Tweet](https://twitter.com/Claybight/status/1624457929763205120))