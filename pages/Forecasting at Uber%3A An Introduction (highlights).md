title:: Forecasting at Uber: An Introduction (highlights)
author:: [[Franziska Bell, Slawek Smyl]]
full-title:: "Forecasting at Uber: An Introduction"
category:: #articles
url:: https://eng.uber.com/forecasting-introduction/

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- quantitative forecasting approaches can be grouped as follows: model-based or causal classical, statistical methods, and machine learning approaches.
	- When the underlying mechanisms are not known or are too complicated, e.g., the stock market, or not fully known, e.g., retail sales, it is usually better to apply a simple statistical model. Popular classical methods that belong to this category include ARIMA (autoregressive integrated moving average), exponential smoothing methods, such as Holt-Winters, and the Theta method, which is less widely used, but performs very well. In fact, the Theta method won the M3 Forecasting Competition, and we also have found it to work well on Uber’s time series (moreover, it is computationally cheap).