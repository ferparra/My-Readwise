title:: Balancer V2: Generalizing AMMs (highlights)
author:: [[medium.com]]
full-title:: "Balancer V2: Generalizing AMMs"
category:: #articles
url:: https://medium.com/balancer-protocol/balancer-v2-generalizing-amms-16343c4563ff

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- Balancer V2 separates the Automated Market Maker (AMM) logic from the token management and accounting. Token management/accounting is done by the vault while the AMM logic is individual to each pool.
		- **Tags**: #[[favorite]]
	- With Balancer's new Protocol Vault, even though trades are carried out in batches against multiple pools, only the final net token amounts are transferred from and to the vault, saving a significant amount of gas in the process.