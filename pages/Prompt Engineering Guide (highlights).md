title:: Prompt Engineering Guide (highlights)
author:: [[promptingguide.ai]]
full-title:: "Prompt Engineering Guide"
category:: #articles
url:: https://www.promptingguide.ai/introduction/settings

- Highlights first synced by [[Readwise]] [[Apr 13th, 2023]]
	- **Temperature** - In short, the lower the `temperature` the more deterministic the results in the sense that the highest probable next token is always picked. Increasing temperature could lead to more randomness encouraging more diverse or creative outputs. We are essentially increasing the weights of the other possible tokens. In terms of application, we might want to use a lower temperature value for tasks like fact-based QA to encourage more factual and concise responses. For poem generation or other creative tasks, it might be beneficial to increase the temperature value. ([View Highlight](https://read.readwise.io/read/01gxhj87npe3fe5qvg32rv89nf))
	- **Top_p** - Similarly, with `top_p`, a sampling technique with temperature called nucleus sampling, you can control how deterministic the model is at generating a response. If you are looking for exact and factual answers keep this low. If you are looking for more diverse responses, increase to a higher value. ([View Highlight](https://read.readwise.io/read/01gxhj8aeqp9hrf80bfkgckcja))