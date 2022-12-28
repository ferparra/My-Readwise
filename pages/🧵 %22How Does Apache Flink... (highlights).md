title:: 🧵 "How Does Apache Flink... (highlights)
author:: [[@gunnarmorling on Twitter]]
full-title:: "🧵 "How Does Apache Flink..."
category:: #tweets
url:: https://twitter.com/gunnarmorling/status/1606265511255281664

- Highlights first synced by [[Readwise]] [[Dec 24th, 2022]]
	- 🧵 "How does Apache Flink compare to Kafka Streams?"
	  
	  Both do stream processing, but differ in some important aspects. A few folks asked me about this recently, so I thought I'd share some thoughts. This is from a user's perspective, not touching on implementation details. 1/10 ([View Tweet](https://twitter.com/gunnarmorling/status/1606265511255281664))
		- **Note**: Thread
	- 1⃣ Supported Streaming Platforms
	  
	  Being part of the @apachekafka project, Kafka Streams exclusively supports stream processing of data in Kafka. @ApacheFlink is platform-agnostic and lets you process data in Kafka, AWS Kinesis, Google Cloud Pub/Sub, RabbitMQ, etc. 2/10 ([View Tweet](https://twitter.com/gunnarmorling/status/1606265515571232768))
	- 2⃣ Deployment Model
	  
	  Kafka Streams is a library which you embed into your Java (or more generally, JVM-based) application. Flink can be used that way, too, but more typically it is run as a cluster of workers to which you upload your jobs. It comes with a web console for... 3/10 ([View Tweet](https://twitter.com/gunnarmorling/status/1606265519761330176))
	- ... managing jobs, dashboards, a REST API, means of auto-scaling ("reactive mode"), a Kubernetes operator, etc. All this helps with running stream processing jobs at scale in prod, whereas with Kafka Streams you'd have to add such an operational layer yourself. This also... 4/10 ([View Tweet](https://twitter.com/gunnarmorling/status/1606265525004296195))
	- ...reflects in the availability of a number of fully managed service offerings for and/or based on Apache Flink.
	  
	  3⃣ Interfaces/APIs
	  
	  Kafka Streams is a Java API exclusively (actually, two: Streams + Processor API); in comparison, ... 5/10 ([View Tweet](https://twitter.com/gunnarmorling/status/1606265527831330816))
	- ... Flink provides two Java APIs (DataStream and Table) as well as one for Python (PyFlink) and a built-in SQL interface (Flink SQL). The latter is fully open-source and part of the Apache Flink project itself, unlike #ksqlDB over in Kafka land. 6/10 ([View Tweet](https://twitter.com/gunnarmorling/status/1606265531350192130))
	- 4⃣ Batch vs. Streaming
	  
	  Kafka Streams focuses exclusively on stateful processing of unbounded data streams, while Flink aims to provide a uniform platform for processing bounded jobs ("batch") and unbounded jobs ("streaming"). 7/10 ([View Tweet](https://twitter.com/gunnarmorling/status/1606265534873341957))
	- 5⃣ Connector Integration
	  
	  Source and sink connectors are a core element of Flink jobs, i.e. they are deployed to the same cluster as the stream processing logic. With Kafka Streams, connectors are deployed and operated separately via Kafka Connect clusters. 8/10 ([View Tweet](https://twitter.com/gunnarmorling/status/1606265537771741185))
	- Those are the key differences between Kafka Streams and Flink from a user's perspective I've found so far, as I'm diving into Flink and its ecosystem. Both have their pros and cons; so as always, you should choose based on your specific context and requirements. 9/10 ([View Tweet](https://twitter.com/gunnarmorling/status/1606265540628070400))
	- Which one of the two (or something else yet?) do you use for stream processing, and why? Any other differences between Flink and Kafka Streams which are worth being called out? Please let me know in the replies 🙏!
	  
	  ~~Fin ~~ 10/10 ([View Tweet](https://twitter.com/gunnarmorling/status/1606265544134361088))
	- @mrhopko @Decodableco In regards to where to get started with Flink, of course I'm biased, but I actually think Decodable is one of the easiest ways: no need to deal with operations, using SQL rather than imperative programming. Besides that, the playground is great: https://t.co/bwtmW5YSSL ([View Tweet](https://twitter.com/gunnarmorling/status/1606333877555007498))