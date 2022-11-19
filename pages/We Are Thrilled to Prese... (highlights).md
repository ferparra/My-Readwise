title:: We Are Thrilled to Prese... (highlights)
author:: [[@LidoFinance on Twitter]]
full-title:: "We Are Thrilled to Prese..."
category:: #tweets
url:: https://twitter.com/LidoFinance/status/1420038063150047236

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- We are thrilled to present a detailed overview of Lido’s road to decentralization. 
	  
	  In this post, we explain the thoughts that led to Lido’s current design and how we plan on transitioning Lido to a piece of fully trustless infrastructure.
	  
	  https://t.co/zXLTqBfDRm ([View Tweet](https://twitter.com/LidoFinance/status/1420037981386199046))
		- **Note**: Thread
	- Even before Ethereum introduced PoS, we predicted that staking would have several friction points, and we wouldn’t be the only ones trying to solve them. 
	  
	  ![](https://pbs.twimg.com/media/E7T6Nm4WEAQyRFG.png) ([View Tweet](https://twitter.com/LidoFinance/status/1420037987426054148))
	- The obvious contenders are centralized exchanges. However, exchanges are already among the largest users of Ethereum; making them the largest block producers could harm decentralization.
	  
	  At Lido, we want to offer a trustless alternative that respects Ethereum’s decentralization. 
	  
	  ![](https://pbs.twimg.com/media/E7T6Wl-XEAI74VD.jpg) ([View Tweet](https://twitter.com/LidoFinance/status/1420038004073189383))
	- However, technical constraints made it impossible to create a fully trustless staking provider when the Beacon Chain launched.
	  
	  We had to choose between a) delaying our launch or b) providing the best possible alternative to exchange staking while minimizing the trust required. ([View Tweet](https://twitter.com/LidoFinance/status/1420038007386779664))
	- Because waiting would have ceded the playing field to exchanges, we deemed an iterative approach would allow us to compete with exchange staking and capture market share while continually reducing trust in the system as the possibilities for it become available. ([View Tweet](https://twitter.com/LidoFinance/status/1420038009521643530))
	- So, what are the key factors preventing a fully trustless staking pool and derivative today? Right now, we can identify three main points where users need to trust Lido. 
	  
	  ![](https://pbs.twimg.com/media/E7T6kJdXIAEUuni.jpg) ([View Tweet](https://twitter.com/LidoFinance/status/1420038014391263232))
	- Subsequently, we discuss what changes to Ethereum & Lido are necessary to support a fully trustless staking pool and derivative. ([View Tweet](https://twitter.com/LidoFinance/status/1420038016995889157))
	- Solution 1: Transitioning custody to a smart contract
	  
	  When we launched Lido, only a BLS address but not an Ethereum address could own a validator. ([View Tweet](https://twitter.com/LidoFinance/status/1420038020175220739))
	- This changed with the introduction of the 0x01 withdrawal credentials. Following that, we updated our withdrawal credentials for new deposits to a smart contract.
	  
	  https://t.co/2Bx58zATYD ([View Tweet](https://twitter.com/LidoFinance/status/1420038022297493507))
	- To switch existing validators to the new address format, we would either need:
	  
	  1) Withdrawals from the Beacon Chain to be enabled, so deposits can be unstaked & restaked.
	  
	  2) A mechanism to rotate validator credentials in-flight. ([View Tweet](https://twitter.com/LidoFinance/status/1420038025330020352))
	- Solution 2: Forcing a validator to unstake remotely
	  
	  If a user wanted to unstake today, Lido would have to issue a message to the validator. That validator then has to unstake manually, allowing them to grief or even extort Lido. ([View Tweet](https://twitter.com/LidoFinance/status/1420038027561291780))
	- Ideally, we would completely solve the problem by allowing stETH holders to trigger a withdrawal from the Beacon Chain remotely. 
	  
	  Recently, Ethereum researchers have made a new proposal that would enable the delegator to force their delegate to unstake. 
	  
	  https://t.co/dWszZ9SlJE ([View Tweet](https://twitter.com/LidoFinance/status/1420038029725552646))
	- Solution 3: Opening up the registry
	  
	  That leaves us with the question of who is allowed to be a node operator for Lido.
	  
	  First, why does Lido need to control who can be a node operator? ([View Tweet](https://twitter.com/LidoFinance/status/1420038031952818184))
	- A core part of Lido’s value proposition is liquid staking, so the issuance of the stETH derivative against a user’s deposit.
	  
	  In a naive implementation, derivatives issued against different validators should trade at different prices as they vary in performance and reliability. ([View Tweet](https://twitter.com/LidoFinance/status/1420038034171568134))
	- However, the resulting tokens wouldn’t be fungible against each other, making it harder to build liquidity for them. 
	  
	  Lido users get issued the same fungible stETH token from their deposit, allowing exchanges, lending markets, etc., to adopt it. ([View Tweet](https://twitter.com/LidoFinance/status/1420038036339970050))
	- This fungibility, while highly desirable, creates a new problem of its own: it requires us to socialize the performance and slashing-risk of bad validators across all stETH holders instead of just the holder of the individual validator’s derivative. 
	  
	  ![](https://pbs.twimg.com/media/E7T7SRfXMAAUDAq.png) ([View Tweet](https://twitter.com/LidoFinance/status/1420038042744725510))
	- This central “quality control” of stakers is a non-trivial problem. In the post, we discuss a non-exhaustive list of possible solutions, ranging from
	- The optimal solution could combine many of the above ideas into one node operator scoring system, where the chance to receive ETH from a new deposit or withdraw ETH for a withdrawal request depends on that operator’s reputation. ([View Tweet](https://twitter.com/LidoFinance/status/1420038048738418688))
	- Node operators would start with a low score but earn points for actions that induce trust from stakers, such as
	- In either case, whatever the optimal solution to opening up the registry is, Lido is committed to finding and implementing it to the best of our abilities. ([View Tweet](https://twitter.com/LidoFinance/status/1420038053641478148))
	- To summarize, we believe the winning Ethereum staking pool and derivative will be a maximally decentralized and immutable protocol, and this is the optimal end state for Lido. ([View Tweet](https://twitter.com/LidoFinance/status/1420038055877136389))
	- We are on track to making Lido fully non-custodial and trustless for stETH holders. Our two top priorities have clear technical solutions that we’re working on with Ethereum developers or waiting to deploy when it’s possible to do so. ([View Tweet](https://twitter.com/LidoFinance/status/1420038058372698115))
	- Trustless entry for node operators is a more complicated problem to solve. Still, we will explore the solutions above and others we haven’t thought about to reduce Lido's reliance on governance as much as possible. ([View Tweet](https://twitter.com/LidoFinance/status/1420038060817924100))
	- We’re committed to iterating quickly and reducing the trust required in Lido as better solutions become available.
	  
	  We’re proud to have offered a better alternative to centralized exchange staking and led the way to build fully decentralized, trustless staking derivatives. ([View Tweet](https://twitter.com/LidoFinance/status/1420038063150047236))