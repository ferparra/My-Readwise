title:: Modern ML Research Loves... (highlights)
author:: [[@marktenenholtz on Twitter]]
full-title:: "Modern ML Research Loves..."
category:: #tweets
url:: https://twitter.com/marktenenholtz/status/1503702562171629570

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Modern ML research loves to ignore time series forecasting.
	  
	  Sure, language sequence modeling is huge, but forecasting isn’t.
	  
	  Yet, for every company in the US’s $5,000,000,000,000 retail industry, forecasting is a huge problem.
	  
	  Here’s your state-of-the-art forecasting toolbox: ([View Tweet](https://twitter.com/marktenenholtz/status/1503702562171629570))
		- **Note**: Thread
	- 1. EDA
	  
	  The best way to start any ML problem.
	  
	  Here are some things to look at in time series data:
	  
	  • Seasonality (monthly, daily, etc.)
	  • Trends (big for proper evaluation)
	  • Autocorrelation
	  • Diff. between older and newer series
	  • Tons of raw samples ([View Tweet](https://twitter.com/marktenenholtz/status/1503702565128597506))
	- 2. Benchmarking
	  
	  Predicting the mean is decent, but keep in mind that even a naive forecaster could outperform that usually.
	  
	  Try things that better consider the domain, such as a rolling mean, predicting the value seen in the last day of available data, etc. ([View Tweet](https://twitter.com/marktenenholtz/status/1503702567863271429))
	- 3. Domain expertise
	  
	  If available, ALWAYS engage with someone that understands how the data is collected and dynamics at play from the business side.
	  
	  There can be huge spikes caused by collection issues, strikes, out of stocks, you name it.
	  
	  These conversations are invaluable. ([View Tweet](https://twitter.com/marktenenholtz/status/1503702570614677508))
	- 4. Model evaluation
	  
	  Any answer other than roll-forward/expanding window cross-validation is wrong for 99.999% of problems.
	  
	  Do NOT do any sort of random split on your samples that doesn’t ensure future values aren’t included.
	  
	  That’s a death sentence for a model. ([View Tweet](https://twitter.com/marktenenholtz/status/1503702573387182080))
	- 5. Now, we're gonna get into the fun stuff: modeling techniques!
	  
	  With the modeling approaches I'll talk about, the following are almost always true:
	  
	  • Don't create group-level models. Make the group a feature ([View Tweet](https://twitter.com/marktenenholtz/status/1503702576121847820))
	- LightGBM/XGBoost
	  
	  You're probably not going to do better than this.
	  
	  For these models, rolling/lag features on the target variable work fantastically.
	  
	  Other great features include grouped aggregations -- this is how you help the model distinguish different groups in the data. ([View Tweet](https://twitter.com/marktenenholtz/status/1503702578860724227))
	- LSTMs/GRUs/Transformers
	  
	  If you have enough data and spend enough time tuning the model, you can beat LightGBM/XGBoost sometimes.
	  
	  The same feature engineering techniques work, but keep in mind that these models are much more finicky about the scale of the data. ([View Tweet](https://twitter.com/marktenenholtz/status/1503702581637353472))
	- 6. Production
	  
	  The main concern you'll have is data drift. Make sure you have a monitoring system that you check in with on a regular basis.
	  
	  Personally, I love adversarial validation to identify data drift. It's one of the most powerful and underused techniques in ML. ([View Tweet](https://twitter.com/marktenenholtz/status/1503702584367869954))
	- Topic TL;DR
	  
	  1. Domain-specific EDA
	  2. Domain-specific benchmarking
	  3. Stakeholder relationships for anomalies
	  4. Model evaluation
	  5. Use XGBoost/LightGBM/RNNs/Transformers
	  6. Monitoring in production ([View Tweet](https://twitter.com/marktenenholtz/status/1503702587098378241))
	- I hope you learned something!
	  
	  Time series modeling is ridiculously important, and knowledge on how to supercharge it is sorely lacking out there in the wild.
	  
	  Follow me @marktenenholtz for more high-signal ML content. ([View Tweet](https://twitter.com/marktenenholtz/status/1503702589883379712))