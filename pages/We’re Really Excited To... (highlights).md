title:: We’re Really Excited To... (highlights)
author:: [[@jerryjliu0 on Twitter]]
full-title:: "We’re Really Excited To..."
category:: #tweets
url:: https://twitter.com/jerryjliu0/status/1625531409137041409

- Highlights first synced by [[Readwise]] [[Feb 16th, 2023]]
	- We’re really excited to introduce a new index type to @gpt_index: a Knowledge Graph 🧠 index! Build a KG by extracting triplets, and leverage the KG during query-time.
	  
	  This index was inspired by @varunshenoy_’s great work on #GraphGPT. See below for how it works 👇 
	  
	  ![](https://pbs.twimg.com/media/Fo8LG4TakAEXTFP.png) ([View Tweet](https://twitter.com/jerryjliu0/status/1625531409137041409))
		- **Note**: Thread
	- We build the index by extracting knowledge triplets in the form (subject, predicate, object), over a set of docs.
	  
	  Each subject and object represents a Node in the graph. We also store references 🔖 from each node to the underlying text. 
	  
	  See an example 🖼️ from @paulg’s essay. 
	  
	  ![](https://pbs.twimg.com/media/Fo8Lgd2agAIOQz4.png) 
	  
	  ![](https://pbs.twimg.com/media/Fo8LhPAaAAAccE-.png) ([View Tweet](https://twitter.com/jerryjliu0/status/1625531410508562432))
	- During query-time, we have two options: 1) query using just the KG as context, or also 2) leverage the underlying text from each entity as context.
	  
	  A simple example with (1) is given below: 
	  
	  ![](https://pbs.twimg.com/media/Fo8LkZsaQAID4T4.png) ([View Tweet](https://twitter.com/jerryjliu0/status/1625531411863326721))
	- With (2), we can ask more complicated queries with respect to the contents of the document. 
	  
	  Since the essay is about the author’s experience at Interleaf, we can ask questions about that even if the KG doesn’t explicitly contain that info! 
	  
	  ![](https://pbs.twimg.com/media/Fo8LnU-aYAECXK1.png) ([View Tweet](https://twitter.com/jerryjliu0/status/1625531413213884416))
	- It is pretty simple to visualize the graph as well. Take a look at the sample code + visualizations below! https://t.co/qqFP9JDM3Z
	  
	  If you want to play around with this, check out our sample notebook 📓 here! Some of this is WIP, very open to feedback 🙂 
	  
	  ![](https://pbs.twimg.com/media/Fo8LrkfaAAE0ciR.png) 
	  
	  ![](https://pbs.twimg.com/media/Fo8LsRSaUAA_qSy.png) ([View Tweet](https://twitter.com/jerryjliu0/status/1625531414543491077))