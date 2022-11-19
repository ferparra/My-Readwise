title:: Platform Thinking —  a Lemonade Case Study // Orr Shilon // MLOps Coffee Sessions #79 (highlights)
author:: [[MLOps.community]]
full-title:: "Platform Thinking —  a Lemonade Case Study // Orr Shilon // MLOps Coffee Sessions \#79"
category:: #podcasts

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- How to Train Models With Cloudre Orces
	  
	  Summary:
	  The platform provides a what we call point in time data. It basically provides dataan on our data warehouse, directly in snowflake. And if researchers want to do maybe explortory data analysis, they can do that directly on the data warehouse  on these giant dimension tables with hundreds of features already been created for them. The most important step for us is that we translate modelling code, both for training and for inference, into our internal platform framework which kind of democratizes training.
	  
	  Transcript:
	  Speaker 1
	  Yes. A, so the platform sort of provides a what we call point in time data, or it basically provides dataan on our data warehouse, directly in snowflake. And if researchers want to do maybe explortory data analysis, they can do that directly on the data warehouse on this lake, on these giant dimension tables with hundreds of features that have already been created for them, or they do it on raw data. Ah, i think at this point we have maybe 15 hundred features in our feature store. So we're at the point where hopefully, a, researchers will be able to not, a, not have to create features for new models, or maybe have to create only several. And then they'll start therea, they'll do their modelling in a note book. And then ike, the most important step for us is that we translate, a, we translate modelling code, both for training and for inference, into our internal platform framework, which kind of democratizes training. So anyone can i train anyone else's model. We have a slack bot to be able to train models with cloudre orces, so we can find a run training there, configure a con figure like a periodic training as well.
	  
	  Speaker 2
	  That's super cool. ([Time 0:10:20](https://share.snipd.com/snip/f61762e3-8fdd-49d9-806b-7bcf117f456e))
	- Is it a Cobernett Service?
	  
	  Summary:
	  All mine feature stores backed by dynamo d b and off liing one, like ast by snowflake. We use am flow both for experiment tracking and as a model repository. And the workflow management that we use as airflow, which is also does, like our periodic training if we need. Its implemented python a. It uses different there are different contexts that it runs init doesit reach streams with lamda ikw slamda a. The system serves real time features from a cobernett service with the fastapi framework.
	  
	  Transcript:
	  Speaker 1
	  Its implemented python a. It has, it uses like different there are different contexts that it runs init doesit reach streams with lamda ikw slamda a. It runs ike. It serves real time features from a cobernett service with the fast api framework. We recently ported, like all for co to a synchronis til i cod have that loop, which has been very successful for us in terms of a model serving latency. Ah, e, all mine feature stores backed by dynamo d b and off liing one, like ast by snowflake. And then we also run like, different tels over coubernets as well. And the workflow management that we use as airflow, which is also does, like our periodic training if we need. And then illl also manage, like, the different etels, if we want to do back congestion into the feature store. We use am flow both for experiment tracking and as a model repository. And we're very heavy on like, a intr structure as a code. So ([Time 0:21:47](https://share.snipd.com/snip/55b8f88c-a9ea-4fe9-9965-86bd880da640))