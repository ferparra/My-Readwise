title:: Principal Component Analysis: Pictures, Code and Proofs (2018) | Hacker News (highlights)
author:: [[news.ycombinator.com]]
full-title:: "Principal Component Analysis: Pictures, Code and Proofs (2018) | Hacker News"
category:: #articles
url:: https://news.ycombinator.com/item?id=19356584

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- There's a running gag at the local polytechnic: All the engineering fields have one thing in common – you measure data, put it into a matrix, calculate its covariance matrix and find the eigenvectors and eigenvalues.
	- PCA works under the assumption that you're dealing with a low-dimensional signal that was projected into a high-dimensional space and then corrupted by low-magnitude high-dimensional noise. By taking only the top k components, you filter out the noise and get a better signal. But if you have a low-magnitude high-dimensional signal corrupted by highly-correlated noise, then naively applying PCA will filter out the signal and leave you with only noise.