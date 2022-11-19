title:: 1/ With @optimismPBC And... (highlights)
author:: [[@bkiepuszewski on Twitter]]
full-title:: "1/ With @optimismPBC And..."
category:: #tweets
url:: https://twitter.com/bkiepuszewski/status/1430790080420003842

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- 1/ With @optimismPBC and @arbitrum likely destined to attract massive TVL soon, we must address the elephant in the room and ask ourselves how safe is the  the fraud proof system for any optimistic rollup 🧵👇 ([View Tweet](https://twitter.com/bkiepuszewski/status/1430790080420003842))
		- **Note**: Thread
	- 2/ Common voiced concern is whether there are incentives for anyone to validate the state commits. IMO this is a non-issue - a lot of parties supporting fast withdrawal schemes will be running L2 full nodes w/out the need for additional incentives from rollups ([View Tweet](https://twitter.com/bkiepuszewski/status/1430790082034900992))
	- 3/ In other words - we will be watching Sequencers. And we are supposed to submit a fraud proof to L1 if we find Sequencer cheating. But fraud proof adjudicator contract is a highly complex piece of software (check solidity code if you are in doubt) ([View Tweet](https://twitter.com/bkiepuszewski/status/1430790083549048833))
	- 4/ How can we be sure that it is bug free ? Will it always, for every state commit, say NO if the state commit is fraudulent and YES is the state commit is correct ? ([View Tweet](https://twitter.com/bkiepuszewski/status/1430790085113520132))
	- 5/ Sequencer is strongly incentivised to be honest. It may submit honest state commits for months. Or years. Until everybody is lulled into the safety and it does not. We need a mechanism to be reasonably assured that when it happens, fraud proofs actually work ([View Tweet](https://twitter.com/bkiepuszewski/status/1430790086589825024))
	- 6/ One way of doing it is to ask Sequencer to submit fraudulent state commit once in a while. But that is a horrible idea from user's perspective. It is as if once in a month we planted a bomb in a shopping centre to test our anti-terrorist squads. But if they fail, many die ! ([View Tweet](https://twitter.com/bkiepuszewski/status/1430790088217276418))
	- 7/ Testing fraud-proof system on a testnet is not that good either - there's no value there, not a lot of people pay attention, certainly not end users - nobody can be sure what has been (if anything) tested there ([View Tweet](https://twitter.com/bkiepuszewski/status/1430790089865580545))
	- 8/ What if Sequencer periodically produced two state commits - one that it claims to be correct and one (from time to time) that it claims to be wrong ? The correct one will be used for withdrawals, but the wrong one will have a bounty for anyone that submits the fraud proof ([View Tweet](https://twitter.com/bkiepuszewski/status/1430790091501457414))
	- 9/ This way we may have watchtowers submitting these fraud proofs and regularly checking that the implementation of the adjudicator actually works. Bounty cost would have to be covered by L2 protocol fees and can be seen as its security budget ([View Tweet](https://twitter.com/bkiepuszewski/status/1430790094026387456))