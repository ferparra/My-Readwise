title:: Dimensionality Reduction in Neural Data Analysis (highlights)
author:: [[xcorr.net]]
full-title:: "Dimensionality Reduction in Neural Data Analysis"
category:: #articles
url:: https://xcorr.net/2021/07/26/dimensionality-reduction-in-neural-data-analysis/

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Visualization: humans are not good at visualizing more than 2 or 3 dimensions. Compressing information down to a handful of meaningful dimensions makes it more feasible to plot them, and understand the factors of variations in the data visually.
	- Denoising: if we want to understand what happens during single trials, we need to denoise the data. If 100 neurons are 100 independent manifestations of the same latent variable, we can boost the signal-to-noise ratio by a factor √100 = 10 by averaging. Dimensionality reduction flexibly averages multiple overlapping realizations of the same data to achieve a boost in signal-to-noise ratio.