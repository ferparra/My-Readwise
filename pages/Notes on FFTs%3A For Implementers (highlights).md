title:: Notes on FFTs: For Implementers (highlights)
author:: [[The ryg blog]]
full-title:: "Notes on FFTs: For Implementers"
category:: #articles
url:: https://fgiesen.wordpress.com/2023/03/19/notes-on-ffts-for-implementers/
document_note:: This document offers suggestions on how to best implement FFTs. It explains the different variants of FFTs, including DIT FFTs, radix-2 and radix-4 decomposition, and split-radix. It also discusses the advantages of larger radices over smaller radices for memory operations, and suggests using iterative FFTs for small sub-FFTs and recursive FFTs for larger sizes. Lastly, it recommends radix-4 (or radix-22) over radix-2 because it has fewer passes and fewer loads/stores.
tags:: #[[math]]

- Highlights first synced by [[Readwise]] [[Mar 24th, 2023]]
	- All Cooley-Tukey family algorithms come in two dual variants, Decimation-in-Time vs. Decimation-in-Frequency. With the recursive decomposition as introduced by Gentleman and Sande, a DIT FFT for even N is decomposed into first computing two size-N/2 DFTs on the even and odd elements respectively. These two DFTs on the even and odd halves of the data can then be combined into a DFT for all N samples by first multiplying the odd-half coefficients by so-called “twiddle factors” and then adding and subtracting the even and twiddled odd halves from each other (“butterflies”). ([View Highlight](https://read.readwise.io/read/01gw9akw40gef4zz3hfkp59d94))