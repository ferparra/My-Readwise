title:: ChatGPT Dec 15 Version (highlights)
author:: [[openai.com]]
full-title:: "ChatGPT Dec 15 Version"
category:: #articles
url:: https://chat.openai.com/chat

- Highlights first synced by [[Readwise]] [[Dec 18th, 2022]]
	- There are several ways a backend engineer can store finite state machines (FSMs) on a database and create a business rule engine. Here are a few approaches you could consider:
	  
	  1.  Store FSMs as a directed graph in the database: You can represent the states and transitions of an FSM as a directed graph in the database, with nodes representing states and edges representing transitions between states. To create a business rule engine, you can then implement a query or script that traverses the graph and applies the relevant rules at each state.
	    
	  2.  Use a library or tool designed for managing FSMs: There are various libraries and tools available that are designed specifically for storing and managing FSMs. For example, the XState library is a popular JavaScript library for building, interpreting, and executing FSMs. You could use a library like this to store the FSMs in your database and create a business rule engine based on the rules defined in the FSMs.
	    
	  3.  Use a workflow engine: A workflow engine is a tool that allows you to define and manage workflows or processes. Many workflow engines support the creation of FSMs, and some even provide visual editors for building them. You could use a workflow engine to store FSMs in your database and create a business rule engine based on the rules defined in the FSMs.
	    
	  4.  Use a NoSQL database: NoSQL databases, such as MongoDB, are designed to store large amounts of unstructured data. You could use a NoSQL database to store the states and transitions of an FSM as a document, and then use the database's query language to implement the business rule engine.
	    
	  
	  Ultimately, the best approach will depend on the specific requirements of your application and the tools and technologies you are using. ([View Highlight](https://read.readwise.io/read/01gmh90q357sp7mg6pyq9yd0je))
		- **Tags**: #[[xstate library]] #[[finite state machine]] #[[programming]]
- New highlights added [[Dec 18th, 2022]] at 6:31 PM
	- Business context: We are a travel insurance company where users select a list of destinations that determine the pricing for their policy. Selecting destinations is at the start of the quotation workflow. Problem to be solved: - Many users struggle at the start because the workflow prompts them to select destinations by country, by city, or by region. In effect, some users who want to travel to a specific region of Indonesia select such country and then can't find the region they are flying to. - If users happen to fly to multiple locations (e.g., do multiple cities in Europe) then they would have to select every single city in their itinerary. This is a friction point in the workflow, and it provides less flexibility (e.g., if I fly to Europe, I would like, as a user, to have a policy that covers me for all of Europe, not having to select all of the cities during my purchasing decision). - The user experience is not clear as what the definition of a destination is, and how it relates to the policy cover. It goes against one of the core business values of being transparent. Idea: How might we make the workflow simpler and easier to use so that users can make a selection based on popular destinations while providing them with flexibility and re-assurance that they are selecting the right selections during their policy purchase? Summarize the text above in one paragraph. ([View Highlight](https://read.readwise.io/read/01gmj1sdwbyrz8e3z3eaa71x90))