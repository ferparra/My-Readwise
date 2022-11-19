title:: Introducing Event Storming (highlights)
author:: [[ziobrando.blogspot.com]]
full-title:: "Introducing Event Storming"
category:: #articles
url:: http://ziobrando.blogspot.com/2013/11/introducing-event-storming.html

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- Some events are the direct consequence of a user action —> represent it as a Command using a blue sticky note
	- Others are the consequence of something happening in external systems or of the time passing, we’ll use a purple sticky note for them
	- we’ll have events that will be the direct consequence of some other events
	- Aggregate is the portion of the system that receives commands and decides whether to execute them or not, thus producing a domain event.
		- **Tags**: #[[favorite]]
	- Exploring Bounded Contexts: during the discussion, some conflict areas might emerge. Developers and facilitators with a DDD mindset will spot different interpretations of terms, as a trigger for discussion around the meaning. This might be a good moment to draw the boundaries between the multiple consistent models that will coexist in your domain.
	- the resulting model is a lot closer to what they need: this ain’t no data model. The resulting model is fully behavioral