title:: How Uniswap V3 Works, Vi... (highlights)
author:: [[@nutstasher on Twitter]]
full-title:: "How Uniswap V3 Works, Vi..."
category:: #tweets
url:: https://twitter.com/nutstasher/status/1583345837236572161

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- How Uniswap V3 works, visually 🧵
	  
	  I had difficulty understanding some of the Uni-v3 tutorials out there, so I’ll try to explain how concentrated liquidity works visually and by using a simple example. I'll assume you have an understanding of Uni-V2, which is much simpler. ([View Tweet](https://twitter.com/nutstasher/status/1583345837236572161))
		- **Note**: Thread
	- 1/
	  In our example, we’ll be trading a USD($)/DAI pair which has a current price of 1$/DAI.
	  
	  In Uni-V2, the LP wants to provide equivalent amounts of DAI and USD into the pool, let’s say 8$ and 8DAI. 
	  
	  This curve shows the familiar xy=L^2 curve 
	  
	  ![](https://pbs.twimg.com/media/Ffj3zUyUYAAAjyx.jpg) ([View Tweet](https://twitter.com/nutstasher/status/1583345842164944896))
	- 2/
	  In UNI-v3, our LP wants to provide liquidity in a price range of 0.5$/DAI and 1.5$/DAI, but how much USD and DAI do they need to provide for the equivalent L=8? 
	  
	  Since we are bounding the price range, we only need to support the dashed part of the virtual reserves curve. 
	  
	  ![](https://pbs.twimg.com/media/Ffj48Q8UcAAa6VD.jpg) ([View Tweet](https://twitter.com/nutstasher/status/1583345846992613383))
	- 3/ 
	  We can calculate the amount of reserves given L=8 and the price. When the price is 1.5$/DAI, there is 6.53DAI remaining. This means we only actually need 
	  8-6.53=1.47DAI of DAI reserves.
	  
	  Similarly, when the price 0.5$/DAI, we only use 
	  8-5.66=2.34$ of USD reserves. 
	  
	  ![](https://pbs.twimg.com/media/Ffj8wX8VIAAvmJ4.jpg) ([View Tweet](https://twitter.com/nutstasher/status/1583345851639820289))
	- 4/
	  Here, the concentrated liquidity curve is labeled real reserves. It’s the same curve as before but shifted down and to the left. Beyond our price range, it would require negative reserves, so swaps can’t happen past those points. p2 shows our initial deposit calculated earlier 
	  
	  ![](https://pbs.twimg.com/media/FfkDnBvVQAA9y6Q.jpg) ([View Tweet](https://twitter.com/nutstasher/status/1583345856203223040))
	- 5/
	  Now, let’s add another LP#2. They would like to deposit with a price range of 0.8$/DAI - 2$/DAI with L=4.
	  
	  The pictures show two real reserve curves, one for each LP. The upper right diagram plots L as a function of log(price). Remember L is constant in the price range. 
	  
	  ![](https://pbs.twimg.com/media/FfkQoVKVQAEZgAx.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FfkQoWXVsAAvH4Y.jpg) ([View Tweet](https://twitter.com/nutstasher/status/1583345857918734336))
	- 6/
	  To get the market making curve for our pool, we add these curves together. The red squares represent liquidity contributions from LP#1 and orange for LP#2. 
	  
	  Note that for certain price ranges L is constant, ex: between .8 and 1.5 $/DAI, both LPs are active so L=8+4=12. 
	  
	  ![](https://pbs.twimg.com/media/FfkSJF2VsAYlh9P.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FfkSNm2VsAEOUBM.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FfkSNndUYAAwuWC.jpg) ([View Tweet](https://twitter.com/nutstasher/status/1583345862532427776))
	- 7/
	  Now, someone wants to buy 3$ worth of DAI. How much DAI do they get? We can’t just plug into a formula because the MM curve is piecewise as shown above. However, each piece has a constant L. 
	  
	  In our example, we can split this into two steps, one for each piecewise curve. ([View Tweet](https://twitter.com/nutstasher/status/1583345864839307264))
	- 8/
	  In the first calculation, in blue, we can calculate the input/output amounts using just L and the start/end price of the section.
	  
	  The second calculation, in pink, requires calculating the end price first, and then using the same formulas in the first calculation. 
	  
	  ![](https://pbs.twimg.com/media/FfklNhJVUAErjj7.jpg) ([View Tweet](https://twitter.com/nutstasher/status/1583345868463144967))
	- 9/
	  There are many other nuances to the Uni-V3 implementation, namely that an LP can’t arbitrarily set the price range, the boundary must fall on a price tick.
	  
	  And since the number of piecewise curves is indefinite, the implementation must be done iteratively. ([View Tweet](https://twitter.com/nutstasher/status/1583345870778429440))
	- 10/
	  Hope this helped you better understand Uni-v3. If it did, please tell me, so I know people find it useful. Follow if you’re interested in learning about DeFi and for updates on an innovative AMM launching soon. ([View Tweet](https://twitter.com/nutstasher/status/1583345871885717505))
	- 11/
	  Huge props to the genius that created this chart in desmos, one of the best tools for understanding Uni-v3: https://t.co/q0XcK1k8aX. If anybody knows who it is please tag them.
	  
	  Perhaps @danrobinson? ([View Tweet](https://twitter.com/nutstasher/status/1583345872963674112))
	- Tagging some folks who have inspired me
	  @BarryFried1 
	  @ProgrammerSmart 
	  @haydenzadams 
	  @finematics 
	  @ThorHartvigsen 
	  @korpi87 
	  @_Dave__White_ 
	  @tarunchitra 
	  @DazaiCrypto 
	  @PatrickAlphaC 
	  @DefiIgnas 
	  @DeFi_Dad 
	  @DAdvisoor 
	  @resdegen 
	  @Uniswap 
	  @thedefiedge
	  
	  https://t.co/OxEIcHzgn8 ([View Tweet](https://twitter.com/nutstasher/status/1583358306730463234))