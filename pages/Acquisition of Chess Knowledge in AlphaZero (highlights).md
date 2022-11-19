title:: Acquisition of Chess Knowledge in AlphaZero (highlights)
author:: [[en.chessbase.com]]
full-title:: "Acquisition of Chess Knowledge in AlphaZero"
category:: #articles
url:: https://en.chessbase.com/post/acquisition-of-chess-knowledge-in-alphazero

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- “From recorded data, we can see that everyone seemed to play e4 in the 1500s. Over centuries, moves like d4, Nf3 or c4 emerged as credible and fashionable alternatives. When we look at AlphaZero, the picture is flipped. The AlphaZero neural network is initially filled with random as its ‘weights’, and therefore experiments with all possible moves. Only after some rounds of self-play does it figure out that many of those are suboptimal.”
	- AlphaZero’s neural network evaluation function doesn’t have the same level of structure as Stockfish’s evaluation function: the Stockfish function breaks down a position into a range of concepts (for example king safety, mobility, and material) and combines these concepts to reach an overall evaluation of the position. AlphaZero, on the other hand, outputs a value function ranging from -1 (defeat is certain) to +1 (victory is guaranteed) with no explicitly-stated intermediate steps.