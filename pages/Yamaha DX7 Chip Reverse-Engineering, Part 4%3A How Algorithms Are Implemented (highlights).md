title:: Yamaha DX7 Chip Reverse-Engineering, Part 4: How Algorithms Are Implemented (highlights)
author:: [[righto.com]]
full-title:: "Yamaha DX7 Chip Reverse-Engineering, Part 4: How Algorithms Are Implemented"
category:: #articles
url:: http://www.righto.com/2021/12/yamaha-dx7-chip-reverse-engineering.html

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- The Yamaha DX7 digital synthesizer (1983) was the classic synthesizer in 1980s pop music.
	  It uses two custom digital chips to generate sounds with a technique called FM synthesis,
	  producing complex, harmonically-rich sounds.
	  Each note was implemented with one of 32 different patterns of modulation and summing, called algorithms.
	- The idea is that you start with a sine wave (the carrier signal) and perturb it with another signal (the modulating signal). The modulating signal changes the phase (and thus the frequency) of the carrier, creating complex harmonic structures.