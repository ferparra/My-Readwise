title:: 🧵 if You Run @Apachekafk... (highlights)
author:: [[@gunnarmorling on Twitter]]
full-title:: "🧵 if You Run @Apachekafk..."
category:: #tweets
url:: https://twitter.com/gunnarmorling/status/1544398510723932160

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- 🧵 If you run @apachekafka in production, creating clusters, topics, connectors etc. by hand is tedious and error-prone. Better rely on declarative configuration which you put into revision control and apply in an automated way, #GitOps-style. Some tools which help with that: ([View Tweet](https://twitter.com/gunnarmorling/status/1544398510723932160))
		- **Note**: Thread
	- 1⃣ JulieOps (https://t.co/Jje6GeXKZq) by @purbon, which helps you to "automate the management of your things within Apache Kafka, from Topics, Configuration to Metadata but as well Access Control, Schemas". A nice intro in this post by Bruno Costa: https://t.co/7CJ4MEz6mH ([View Tweet](https://twitter.com/gunnarmorling/status/1544398513487941633))
	- 2⃣ topicctl (https://t.co/QtMlEDb0ZD) by @segment: "Easy, declarative management of Kafka topics. Includes the ability to 'apply' topic changes from YAML as well as a repl for interactive exploration of brokers, topics, consumer groups, messages, and more" ([View Tweet](https://twitter.com/gunnarmorling/status/1544398515979313154))
	- 3⃣ #Terraform is a popular tool amongst many infrastructure-as-code adepts. No surprise that there is a TF provider for Kafka resources for it too: https://t.co/piEbKDIUSE. ([View Tweet](https://twitter.com/gunnarmorling/status/1544398518709886980))
	- 4⃣ If #Kubernetes is your thing, take a look at @strimziio (https://t.co/WfAFVhO3EB), an open-source operator for running Kafka on Kube, which lets you manage clusters, topics, users, Connect, connectors, MirrorMaker and others, via custom resources and kubectl. 
	  
	  ![](https://pbs.twimg.com/media/FW6yWJkWIAIFyP6.jpg) ([View Tweet](https://twitter.com/gunnarmorling/status/1544398524762275844))
	- 5⃣ Users of managed Kafka services like MSK, Red Hat's RHOSAK, or Confluent Cloud, usually find GitOps friendly solutions offered by their providers or the community, e.g. via CloudFormation (https://t.co/ockklSBPoR) or TF (https://t.co/qAUXjGtBrF, https://t.co/ockklSBPoR). ([View Tweet](https://twitter.com/gunnarmorling/status/1544398527673008128))
	- 6⃣ And some more tools in the Kafka GitOps/IaC space I've come across: