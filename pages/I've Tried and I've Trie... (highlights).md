title:: I've Tried and I've Trie... (highlights)
author:: [[@jasoncwarner on Twitter]]
full-title:: "I've Tried and I've Trie..."
category:: #tweets
url:: https://twitter.com/jasoncwarner/status/1595485931422638081

- Highlights first synced by [[Readwise]] [[Nov 24th, 2022]]
	- I've tried and I've tried and I've tried but enough people have asked me to comment on what's likely to happen to Twitter *architecturally* so I'll do a reluctant thread
	  
	  *Really* hoping to avoid any other twitter commentary but there is always some overlap ([View Tweet](https://twitter.com/jasoncwarner/status/1595485931422638081))
		- **Note**: Thread
	- 1. Is Twitter likely to go away?
	  
	  No, not from technical problems ([View Tweet](https://twitter.com/jasoncwarner/status/1595485934077853731))
	- 2. Will Twitter suffer technically during this period?
	  
	  Yes, it already is. Even just casual users of Twitter have seen lots of small & medium sized issues pop up the last few weeks. This is just through observation. If you go looking (open up devconsole) you'll find more ([View Tweet](https://twitter.com/jasoncwarner/status/1595485936866902016))
	- And these are literally the lightest way possible to see them. I'm sure api products are suffering much more based on a simple script I ran to test one api
	  
	  This doesn't mean failure is imminent. I'm sure their systems are stressed but .... ([View Tweet](https://twitter.com/jasoncwarner/status/1595485939425386498))
	- 3. Will any of it matter, technically?
	  
	  No, probably not. Why not?
	  
	  It's the nature of the twitter product. Twitter the service can suffer lots and lots and lots of issues and it will still be a useful/amusing service for many. It is not the same as a mission critical product ([View Tweet](https://twitter.com/jasoncwarner/status/1595485941904199680))
	- Ex: GitHub, Heroku, Twilio, Stripe, Okta, Duo, Cloudflare, S3 etc These things go down & entire businesses stop cold, users all around the world in *other* applications stop cold. Basically, the world stops ([View Tweet](https://twitter.com/jasoncwarner/status/1595485944429260800))
	- Twitter is used by hundreds of millions around the world mostly for casual distraction during the day. Sure, some people use it for work etc etc etc, but that's not the main use case
	  
	  And most people are not too on-line like many people reading this thread ([View Tweet](https://twitter.com/jasoncwarner/status/1595485946933223424))
	- The very nature of the twitter product allows twitter the service so much uptime/latency/architectural leeway that no, the faults we've been seeing and likely to see for a while will not cause it to fail. It'll be amusing for some, maybe frustrating for others etc but won't fail ([View Tweet](https://twitter.com/jasoncwarner/status/1595485949487566854))
	- Remember that Twitter, yes a much smaller version of it, survived *years* of the failwhale. Users just don't care the same way they would if GitHub or S3 or Okta is down for even 10 minutes ([View Tweet](https://twitter.com/jasoncwarner/status/1595485952058613760))
	- And also remember that all failures are not created equal and the type of out outage Twitter could suffer that would stop people using it is so different than mission critical services
	  
	  Didn't load a tweet? no one notices
	  
	  Can't load an old thread? people try again ([View Tweet](https://twitter.com/jasoncwarner/status/1595485954596216832))
	- Delete all tweets from 2017 by mistake? Just restore from cold storage...% chance people even notice or care so low
	  
	  Entire app stops working for 24 hours? people distract themselves with another casual thing and then come back and complain about twitter on twitter ([View Tweet](https://twitter.com/jasoncwarner/status/1595485957129523200))
	- The point is the twitter the company is not likely to be taken down by twitter the service not working exactly right for even long long stretches of time ([View Tweet](https://twitter.com/jasoncwarner/status/1595485959683858432))
	- 4. Where can the tech fail twitter?
	  
	  Twitter core service is, for those of us in the dist systems game, really not that hard to build & manage even at scale (this is a relative like saying a windmill dunk isn't that impressive for avg NBA player vs me, who can't dunk anymore) ([View Tweet](https://twitter.com/jasoncwarner/status/1595485962171138049))
	- But it's everything around the service that make up the company where the risk is. These are very very very likely bespoke tools with years of learnings baked into the logic/workflows that *require* the systems to interact a certain way ([View Tweet](https://twitter.com/jasoncwarner/status/1595485964691906565))
	- When all those things fail lots of odd potentially bad or maybe even illegal things can happen. It's also when hackers/nation states etc can have the most opportunity. Chaos is a ladder (game of thrones) & right now is when china and russia would be testing twitter edges the most ([View Tweet](https://twitter.com/jasoncwarner/status/1595485967183278080))
	- 5. "But Jason, I WANT it to matter!"
	  
	  I got nothing for ya here. It's not likely to go away from the tech. It's going to suffer, there will likely be a few outages that get noticed by some folks (likely geos, not global), things will load slower, latencies will increase etc ([View Tweet](https://twitter.com/jasoncwarner/status/1595485969733812224))
	- 6. What could go massively wrong?
	  
	  Well, it's the "there is no way we could have anticipated that" scenario that is can cause internal twitter massive pain
	  
	  See this outage at GitHub: https://t.co/dLBzSnkmnz ([View Tweet](https://twitter.com/jasoncwarner/status/1595485972237459457))
	- Disks filling up, whole server racks getting unplugged, a bad replica being promoted to master, fat finger in prod, bad config etc
	  
	  It's not the normal services that could go wrong....it's when someone needs to debug what is happening IN THE MOMENT with some unexpected situation ([View Tweet](https://twitter.com/jasoncwarner/status/1595485974753968129))
	- This is where GREAT infra teams shine and principles about the business are put to the test. In the above GitHub outage you can see the original fault was corrected in 43 seconds and I got the call about what to do in minutes from @isamlambert. Decisions made in that moment... ([View Tweet](https://twitter.com/jasoncwarner/status/1595485977329381376))
	- are what make & break how things go. Note that in GH's case the original fault was something not at all related to GH, was planned for, but (not all details published) the *reaction* by someone (non-GitHub) at the datacenter wasn't expected, result 43 sec fault, 24 hour outage ([View Tweet](https://twitter.com/jasoncwarner/status/1595485979824881665))
	- In the moment we made a decision (side note: Sam called me when I was on my first family vacation since joining GitHub 18 months before & literally on a mountain in Hawaii w/ spotty cell coverage) to preserve user data at all costs ([View Tweet](https://twitter.com/jasoncwarner/status/1595485982425600000))
	- Twitter doesn't have to make these types of decisions at core services. It has it's own set of critical business decisions &, frankly speaking, it's mostly about the service being mostly available for most people most of the time. We aren't talking 5,4,3 maybe even 2.5 9's here ([View Tweet](https://twitter.com/jasoncwarner/status/1595485985122328576))
	- 7. What's your take on their architecture?
	  
	  A. this type of diagram is mostly helpful for new hires to get 50,000 ft acclimated to systems. It's stops being useful once you know a system. Suspect this was drawn exclusively for Elon and non-infra people to come up to speed https://t.co/ImEUh9GD4F ([View Tweet](https://twitter.com/jasoncwarner/status/1595485987647287296))
	- B. this looks like read, not write. Write is harder to do than read but twitter is majority read service so I get why this is published
	  
	  C. Going down a few levels would be more interesting. Message passing/routing etc is where most of the devil lives in dist systems ([View Tweet](https://twitter.com/jasoncwarner/status/1595485990428082176))
	- D. Nothing is "simple" at scale. So each of those things is only as interesting as one knowing which tradeoffs they are making. Search is always a good example
	  
	  Search is "easy" because you just throw lucene or solr or elastic at it, right?
	  
	  Not at scale ([View Tweet](https://twitter.com/jasoncwarner/status/1595485993120911360))
	- Search is a GREAT example because to the lay person "just make search fast" is what they want but the tradeoffs in it are so massively different. But at what cost...like literal cost. Search is expensive....very expensive to do. You can make it blazing fast for $... ([View Tweet](https://twitter.com/jasoncwarner/status/1595485995612270592))
	- You can also make it fast for less but even that isn't free, it takes bespoke work to get there. Off the shelf x, y, z won't do it in very specific cases and Twitter has some special needs here....or it can do it the expensive way ([View Tweet](https://twitter.com/jasoncwarner/status/1595485998170796032))
	- GitHub famously had meh/bad search for a long time. @p_reynolds decided enough was enough and prototyped the new Code Search (https://t.co/hgHVMtDqlP) specifically for GitHub's use case. He did an amazing job understanding deeply what users needed from GitHub search ([View Tweet](https://twitter.com/jasoncwarner/status/1595486000704147456))
	- But simply "make search fast" isn't all that helpful, or easy, mostly because it's not about "just doing x or y or z" or "throw some lucene and big clusters at it" unless you want to burn hundreds of millions of dollars a year (which could be ok in many cases) ([View Tweet](https://twitter.com/jasoncwarner/status/1595486003258458113))
	- So the point is this apparently read architecture makes sense at the highest level. The next few levels down would be massively more interesting to see how they are doing things, which optimizations/tradeoffs they are making and also assumptions ([View Tweet](https://twitter.com/jasoncwarner/status/1595486005846429696))
	- After that it's all about how faults are handled (& 'faults' is a massive category as simple as increased latency to disk full, database now crashing, replica got triggered to promote, can't reach tier 1 on-call twilio is also down no paging right now) but that is for another day ([View Tweet](https://twitter.com/jasoncwarner/status/1595486008396550144))
	- Not much else to say. I don't think twitter is going away. And I say that adding this line that as I tried to post this it got kicked back and I had to try again. This time it worked. Few minutes in between etc...no big deal...after all this isn't mars mission control ([View Tweet](https://twitter.com/jasoncwarner/status/1595486010946727936))