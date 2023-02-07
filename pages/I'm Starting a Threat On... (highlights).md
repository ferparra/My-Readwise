title:: I'm Starting a Threat On... (highlights)
author:: [[@brunowinck on Twitter]]
full-title:: "I'm Starting a Threat On..."
category:: #tweets
url:: https://twitter.com/brunowinck/status/1592130794419810305

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- I'm starting a threat on the key patterns shared today by several modern PKM/Tft/note-taking apps.
	  
	  I don't mean all apps have them, but it's a good pov to see what progresses have been made in the last 2 years.
	  
	  Feel free to contribute ... ([View Tweet](https://twitter.com/brunowinck/status/1592130794419810305))
		- **Note**: Thread
	- Markdown introduced the ability to add formatting with any text editor. Before that, it was either proprietary rich editors (ala Word, Evernote) with limited interoperability or HTML, which is overkilled in most cases. 
	  
	  A gain of [[interoperability]] but risk of using a non-standard ([View Tweet](https://twitter.com/brunowinck/status/1592130796617625601))
	- Wikilinks, introduced in the https://t.co/w91zzNQyjO , 20 years ago are now common. The idea is that all pages have a name, possibly invented, and referring to them in the text using double brackets makes a link automagically ([View Tweet](https://twitter.com/brunowinck/status/1592130799813681155))
	- Backlinks, first demonstrated in Roam, can be implemented as a search (as it was in https://t.co/w91zzNQyjO) or by maintaining backlinks. 
	  
	  The benefit is to see instantly where a page is referenced and count on it being easy. ([View Tweet](https://twitter.com/brunowinck/status/1592130804989440001))
	- Block level addressability. Before this only named pages could be referenced using name links (aka wikilinks).
	  
	  Worth noting that apps built on top of true knowledge graphs didn't need that because everything was addressable by id. It's more a benefit for document based apps. ([View Tweet](https://twitter.com/brunowinck/status/1592130807082385409))
	- hashtags, mentions, and wikilinks are playing similar roles.
	  
	  This alignment of 3 patterns adds to agility and versatility. 
	  big loosers here are wikinames ( compound names using two uppercases (camelcase). ([View Tweet](https://twitter.com/brunowinck/status/1592130809221480448))
	- Local first. The ability to use the apps exclusively on one's computer with almost no network access. 
	  
	  That doesn't imply the usage is free (a call home can be done like in Notion), or that the data can be accessed directly (like in roam, it stays encrypted, & in the localstore) ([View Tweet](https://twitter.com/brunowinck/status/1592130810957729792))
	- Filesystem first. That's a step further than local first. That's what Obisidian, Logseq (and kneaver notes) do. 
	  
	  Your work is directly accessible by any tool on your disk. 
	  A cache database is built to provide fast search, link resolution, & access. 
	  
	  The most perennial solution ([View Tweet](https://twitter.com/brunowinck/status/1592130813155581953))
	- Outliner. In this pattern, which is still a document-first pattern,  the document (of text type), is broken into a hierarchy of small blocks, and editing happens at the block level.  
	  
	  You can use bullet points & tabs in Obsidian or Evernote, but they are not native outliners. ([View Tweet](https://twitter.com/brunowinck/status/1592131874876715008))
	- One of the brilliant moves from Roam was to make the outliner structure almost frictionless. Navigating the page behaves almost like a plain text editor, but it's really made of blocks.
	  
	  Access control, traceability, and addressability are at the block level. ([View Tweet](https://twitter.com/brunowinck/status/1592134646065934337))
	- This, with the block refs and backlinks, gives the "Lego" UI feeling inside roam. 
	  
	  The drawback is that it's very taxing from a cognitive load pov. You can do everything, but you also must control everything you do. ([View Tweet](https://twitter.com/brunowinck/status/1592134649261735938))
	- Fluid text to structure transition. Introduce by Tana via supertags. It's a partial solution to the fragility mentioned above. You structure your blocks on the go using tags following the mentions. 
	  
	  Since supertags have definitions, it opens the way to keep your work structured. ([View Tweet](https://twitter.com/brunowinck/status/1592134651464019968))
	- Yet it still has very serious limitations compared to knowledge graph systems and neural databases.
	- Schema-defined knowledge base.
	  
	  That's a step many users could find constraining but having schemas in place (person, books, concepts, tools, ...) is the way to keep your PKM under control in the long run. ([View Tweet](https://twitter.com/brunowinck/status/1592134656455241729))
	- Shared schemas and semantic
	  
	  If your tool lets you import directly schemas defined in RDF (skos, foaf) or https://t.co/Q3I1Gh3AOf, you gain a *huge* advantage
	- Short parenthesis to remind us what means a note-taking app WITHOUT links. 
	  
	  You can add URLs in your notes, but they are absolute URLs. 
	  
	  You need to go inside the target note, obtain a link to it, go back to where you want to link, paste and assign a label. 
	  
	  Very tedious. ([View Tweet](https://twitter.com/brunowinck/status/1592168679617462272))
	- Making a link implies opening two notes and an obscure string.
	  
	  The system doesn't make a difference between links inside the vault and outside. 
	  
	  You can't see which notes are related to the note you read. It's like being blind. Which is silly since computers do that easily. ([View Tweet](https://twitter.com/brunowinck/status/1592168684747096068))
	- In some systems, mostly genuine graph-based links can be added *without* touching the source or the target. This is because links are outside of the nodes.
	  
	  Not being able to do it is a sign the model is, in fact, asymmetrical. More a tree or a set of pages than a graph ([View Tweet](https://twitter.com/brunowinck/status/1592273298083442689))
	- There are few pure graph db-based apps today. One of them is @codexeditor based on neo4j, and another is @napkin_ideas. TBH, I never had access to the internals of both. There is another I know very well. ([View Tweet](https://twitter.com/brunowinck/status/1592273302482870274))
	- Strange enough, people with experience in using graph databases for PKM learned that more is needed. To maintain annotations on relations like modality (are we sure of that fact), we need hypergraphs. ([View Tweet](https://twitter.com/brunowinck/status/1592273306341998592))
	- Such hypergraphs are typically recursive, and they support links between links and nodes, and again between those links, etc. we don't need more.
	  
	  A side benefit is that hypergraphs are compatible with strict access control. You can annotate or link something without modifying it ([View Tweet](https://twitter.com/brunowinck/status/1592273309861048320))
	- Since we are in the data model, let's talk of attributes.
	  
	  Most systems allow to define attributes or metadata using the YAML syntax, in a "front matter" manner:
	  AttrName: AttrValue
	  
	  For a book you can set the first published date.
	  
	  First Published: 2021-06-01 ([View Tweet](https://twitter.com/brunowinck/status/1592277766271291393))
	- An extension: Some systems allow us to define relations as attributes. 
	  
	  In a Book:
	  
	  Authors: X, Y, Z 
	  
	  Different nuances exist. Kneaver would propagate the constraint: what is after "Authors" don't need wikilinks or tags, it's assumed that those are persons who wrote books. ([View Tweet](https://twitter.com/brunowinck/status/1592277775808856064))
	- Time to put Notion back on the map. In notion, each record can be seen as a page, each attribute being the fields of the record. Records together form a table.
	  
	  That's true also for systems using schemas. The set of all nodes with a given schema can be seen as a table ([View Tweet](https://twitter.com/brunowinck/status/1592277779525275650))
	- The set of all nodes with type (or schema or kind) "book" form the table of "books".
	  
	  That's very handy because now we have both a graph database and a table database. It let us reconcile very structured data and notes. ([View Tweet](https://twitter.com/brunowinck/status/1592277785019842560))
	- A key difference between a system made of tables like Notion & a more advanced shema-based system like Tana is that we have the inheritance. 
	  
	  A person is an agent
	  An organisation is an agent
	  
	  I can ask the table of Persons, the table of Organisations or the table of Agents. ([View Tweet](https://twitter.com/brunowinck/status/1592277789222531073))
	- On top of that we can have facets, or shapes or aspects.
	  
	  An Author is a facet of Agent (see above) with a list of books. 
	  
	  Now we are equipped to do serious Knowledge Representation. Something Notion can't do AFAIK. ([View Tweet](https://twitter.com/brunowinck/status/1592277793877987331))
	- Let's explore the multi-user side of things.
	  
	  Two problems to solve
	- While we talk about PKM, we don't live on islands and we work with others.
	  
	  Two philosophies
	- The peer-to-peer solution seems to me more sustainable because it removed the responsibility of the central database. 
	  
	  There could be a shared replica somewhere but it becomes optional. ([View Tweet](https://twitter.com/brunowinck/status/1592281580537806849))
	- Next is the access control. 
	  
	  To which level do we define access control.
	- @Kneaver, is old school. Each node has a scope, and scopes can define access control very finely. Even in a shared database, some users can totally ignore the existence of some nodes. Links, wikilinks, & hashtags will not resolve as if they didn't exist.
	  I think it's a good model ([View Tweet](https://twitter.com/brunowinck/status/1592281590809649152))
	- Another set of patterns is extensibility.
	  
	  Roughly saying there are 3 locations for extensibility.
	- Server-side API: 
	  
	  PKM is not an island. You will want to save Twitter threads, save kindle highlights, save emails but also to publish pages, send mailing from your PKM system etc. 
	  
	  Of course, your system could grow & englobe all that but it becomes a dinosaur & we know the end ([View Tweet](https://twitter.com/brunowinck/status/1592286346659471361))
	- So 10 years ago, engineers had a smart idea: every service will offer an [[API]] that other services can connect to. Twitter, Trello, Google, Facebook, Circle everyone did it. 
	  
	  A huge ecosystem was built. it allows interoperability between hundreds of apps. That's what [[Zapier]] uses ([View Tweet](https://twitter.com/brunowinck/status/1592286350447120384))
	- Using other services API allows to build integrations. If the PKM system has an API itself, it allows everyone to build integrations. It's a powerful pattern. 
	  
	  Unigraph has been very successful at that. 
	  
	  @Kneaver has no less than 18 integrations. 
	  
	  So it's possible ([View Tweet](https://twitter.com/brunowinck/status/1592295945915535364))
	- Sadly, MVP & UI first approach of the last generations of apps made that API come very late in the roadmap. One or 2 years is common.
	  
	  Most recent apps are client-side only. It seems this pattern is losing traction. 
	  
	  Down side is that it causes major cognitive load for the users ([View Tweet](https://twitter.com/brunowinck/status/1592295948742688771))
	- The second possibility for extensions is the schema. 
	  
	  That's one reason for the success of Notion. You can build a template (new tables, new layouts) and share it with other users in their own database. 
	  
	  Having standard schemas & possibilities to import them would simplify that ([View Tweet](https://twitter.com/brunowinck/status/1592295951913607169))
	- Finally, the ability to change the UI/UX with extensions. It's totally client-side.
	  
	  One cause of the success of roam was the ecosystem of plugins which grew spontaneously. 
	  
	  It was not in the plans & was out of control, but users were excited to see their desires realized. ([View Tweet](https://twitter.com/brunowinck/status/1592295955180974081))
	- Giving the users and third parties the power the expand the system to silly customization to fill niche needs is a recipe for success. 
	  
	  Why? because the more personal a product is, the more it must be adapted. 
	  
	  Templates are not enough. You need a language, a UI kit etc. ([View Tweet](https://twitter.com/brunowinck/status/1592298445544787968))
	- Let's remember it was the formula for the success of Autocad, a popular 2D CAD system of the 80s. 
	  
	  They picked LISP as the language, and people developed complete applications using it. 
	  
	  The founder, John Walker became rich and sponsored ... Xanadu from Ted Nelson :) ([View Tweet](https://twitter.com/brunowinck/status/1592298453920403456))
	- among the system which implemented well extensions: logseq, obsidian.
	  
	  Roam resisted a long time before eventually coming up with roam depot, but too late. 
	  
	  Another recent app is ignoring this pattern. ([View Tweet](https://twitter.com/brunowinck/status/1592298459109163008))
	- I take a break here, but there is much more to cover: Visual thinking apps, AI.
	  
	  Stay tuned... ([View Tweet](https://twitter.com/brunowinck/status/1592298462682714112))