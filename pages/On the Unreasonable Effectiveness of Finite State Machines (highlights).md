title:: On the Unreasonable Effectiveness of Finite State Machines (highlights)
author:: [[kevmo314.com]]
full-title:: "On the Unreasonable Effectiveness of Finite State Machines"
category:: #articles
url:: https://blog.kevmo314.com/finite-state-machines.html

- Highlights first synced by [[Readwise]] [[Dec 18th, 2022]]
	- type OpenState = "open"; type ClosedState = "closed"; type DoorState = OpenState | ClosedState; ([View Highlight](https://read.readwise.io/read/01gmh99psh4q3xzfrjxpgacw1q))
	- function close(state: OpenState): ClosedState { return "closed"; } function open(state: ClosedState): OpenState { return "open"; } ([View Highlight](https://read.readwise.io/read/01gmh99syw1hp3t0cvf5g14hgd))
	- So finite state machines are just composed of finite state machines. Take this to an extreme and look at a computer. A [von Neumann](https://en.wikipedia.org/wiki/Von_Neumann_architecture) architected computer is composed of memory, which stores state, and a processor, which performs transitions. Therefore, **a physical computer is nothing but a finite state machine.** Functions are nothing but transitions between memory states. And I think this realization is why writing a finite state machine from scratch is so insightful, because viewing code as nothing but state transitions offers a way to dramatically reduce complexity and make code easier to understand. ([View Highlight](https://read.readwise.io/read/01gmh9azxbbywmghzemd3887fz))
		- **Tags**: #[[computing]] #[[finite staet machines]]