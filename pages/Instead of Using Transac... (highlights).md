title:: Instead of Using Transac... (highlights)
author:: [[@gakonst on Twitter]]
full-title:: "Instead of Using Transac..."
category:: #tweets
url:: https://twitter.com/gakonst/status/1547765983598653447

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- instead of using transaction relayers, try running github action cronjobs with forge scripts
	  
	  can automate all your chain ops inside a solidity file that's driven by a GHA that runs periodically, where either GH stores your PK (might be fine for meta tx) or with AWS/GCP KMS ([View Tweet](https://twitter.com/gakonst/status/1547765983598653447))
	- this also applies to other chain ops, e.g. wallet consolidation at the end of the day (send to exchange / tornado / else?)
	  
	  all of this was possible before, but Solidity lowers the barrier to entry / improve the UX (vs writing full scripts) that ppl might actually try it ([View Tweet](https://twitter.com/gakonst/status/1547769285304455168))
	- the reason why forge scripts are very powerful is because they bake in the "crank", the part which handles *submission* & polling of pending transactions, and you just need to specify *what* to send, instead of having to think about ten other things ([View Tweet](https://twitter.com/gakonst/status/1547769601282363393))