title:: Computational Causal Inference at Netflix (highlights)
author:: [[Netflix Technology Blog]]
full-title:: "Computational Causal Inference at Netflix"
category:: #articles
url:: https://netflixtechblog.com/computational-causal-inference-at-netflix-293591691c62

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- Scientists from these fields have made many advancements in causal effects research in the past few decades, spanning instrumental variables, forest methods, heterogeneous effects, time-dynamic effects, quantile effects, and much more. These methods can provide rich information for decision making, such as in experimentation platforms (“XP”) or in algorithmic policy engines.
	- Computation can explode and become overwhelming when this is done with large datasets, with high dimensional features, with many possible actions to choose from, and with many responses.
	- Time dynamic treatment effects are notoriously hard to scale. They require a panel of repeated observations, which generate large datasets. They also contain autocorrelation, creating complications for estimating the variance of the causal effect. How can we make the computation for the time-dynamic treatment effect, and its distribution, more scalable?