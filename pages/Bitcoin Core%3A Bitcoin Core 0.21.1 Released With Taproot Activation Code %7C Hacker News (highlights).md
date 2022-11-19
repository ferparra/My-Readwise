title:: Bitcoin Core: Bitcoin Core 0.21.1 Released With Taproot Activation Code | Hacker News (highlights)
author:: [[news.ycombinator.com]]
full-title:: "Bitcoin Core: Bitcoin Core 0.21.1 Released With Taproot Activation Code | Hacker News"
category:: #articles
url:: https://news.ycombinator.com/item?id=27020002

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- One of the big improvements is that multi-signature transactions, where both Alice and Bob have to sign to spend some money, used to require adding N signatures (number of signers) to the block chain to have a valid transaction. So it improves efficiency and should allow squeezing more transactions, but it also improves privacy, because there's no way to tell if how many parties are involved in the transaction.Merkelised Abstract Syntax Tree (MAST) are the other big feature that allows for more complex scripting to also be represented in a compressed and obfuscated way (example in the link).
		- **Tags**: #[[favorite]]
	- Then, if the parties transacting cooperate they can keep their fancy conditions private and just sign using a single jointly controlled key.  If the parties don't cooperate some of the conditions may need to be exposed, but only the absolute minimum to show the transaction is allowable.  Cooperation is likely however, because non-cooperating won't create a benefit.
	- The effect is that instead of being limited to a few thousand bytes of operations for the rules governing your coin, you could have gigabytes of rules, and yet never expose them (and burn network resources and your privacy) -- or if you do need to to expose some of them, you only need to show a small amount.  ... and as a bonus have your transactions look just like a really boring maximally simple wallet's transactions.