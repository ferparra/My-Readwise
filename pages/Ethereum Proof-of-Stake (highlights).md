title:: Ethereum Proof-of-Stake (highlights)
author:: [[0xfoobar.substack.com]]
full-title:: "Ethereum Proof-of-Stake"
category:: #articles
url:: https://0xfoobar.substack.com/p/ethereum-proof-of-stake

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- A slot occurs every 12 seconds, and exactly one validator is randomly chosen to submit a block within the slot. An epoch is composed of 32 slots, or 6.4 minutes. If a validator is offline and does not propose a block within its slot, that slot is left empty. So Ethereum blocktimes will move from a Poisson distribution with average blocktime of 13 seconds, to exactly 12 seconds with occasional empty slots. The first block within each epoch is treated as the checkpoint block.
	- True protocol-level staking means entering into a commitment with both upside and downside, that requires consistent active participation into proposing new blocks and attesting to blocks others create.
	- PoS solves the nothing-at-stake problem by adding slashing penalties to validators who build on two parent blocks at once.