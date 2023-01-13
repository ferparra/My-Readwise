title:: Chapter 1. Basics of Rust Concurrency (highlights)
author:: [[Mara Bos]]
full-title:: "Chapter 1. Basics of Rust Concurrency"
category:: #articles
url:: https://marabos.nl/atomics/basics.html#threads
tags:: #[[rust]]

- Highlights first synced by [[Readwise]] [[Jan 7th, 2023]]
	- Every program starts with exactly one thread: the main thread. This thread will execute your `main` function and can be used to spawn more threads if necessary. ([View Highlight](https://read.readwise.io/read/01gp4nxv5dgsgztpydw7xvsv7f))
	- In Rust, new threads are spawned using the `std::thread::spawn` function from the standard library. ([View Highlight](https://read.readwise.io/read/01gp4ny04tq785d94nq2wz68y0))