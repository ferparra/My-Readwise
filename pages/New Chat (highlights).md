title:: New Chat (highlights)
author:: [[chat.openai.com]]
full-title:: "New Chat"
category:: #articles
url:: https://chat.openai.com/chat

- Highlights first synced by [[Readwise]] [[Dec 18th, 2022]]
	- There are several ways a backend engineer can store finite state machines (FSMs) on a database and create a business rule engine. Here are a few approaches you could consider:
	  
	  1.  Store FSMs as a directed graph in the database: You can represent the states and transitions of an FSM as a directed graph in the database, with nodes representing states and edges representing transitions between states. To create a business rule engine, you can then implement a query or script that traverses the graph and applies the relevant rules at each state.
	    
	  2.  Use a library or tool designed for managing FSMs: There are various libraries and tools available that are designed specifically for storing and managing FSMs. For example, the XState library is a popular JavaScript library for building, interpreting, and executing FSMs. You could use a library like this to store the FSMs in your database and create a business rule engine based on the rules defined in the FSMs.
	    
	  3.  Use a workflow engine: A workflow engine is a tool that allows you to define and manage workflows or processes. Many workflow engines support the creation of FSMs, and some even provide visual editors for building them. You could use a workflow engine to store FSMs in your database and create a business rule engine based on the rules defined in the FSMs.
	    
	  4.  Use a NoSQL database: NoSQL databases, such as MongoDB, are designed to store large amounts of unstructured data. You could use a NoSQL database to store the states and transitions of an FSM as a document, and then use the database's query language to implement the business rule engine.
	    
	  
	  Ultimately, the best approach will depend on the specific requirements of your application and the tools and technologies you are using. ([View Highlight](https://read.readwise.io/read/01gmh90q357sp7mg6pyq9yd0je))