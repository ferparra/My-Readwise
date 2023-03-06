title:: The Mythical Man-Month: Essays on Software Engineering (highlights)
author:: [[Blas]]
full-title:: "The Mythical Man-Month: Essays on Software Engineering"
category:: #articles
url:: https://blas.com/the-mythical-man-month/
document_note:: The Mythical Man-Month is a book that discusses the difficulties of managing large programming projects due to the division of labor. It suggests that the most important consideration in system design is ease of use, which requires unity of design and conceptual integrity, and proposes the use of top-down design and growing software instead of building it. According to the author, adding more software developers will not make projects on time, and it is important to have as few minds as possible in order to ensure conceptual integrity. The book emphasizes the importance of testing, iteration, and sharp milestones throughout the development process.

- Highlights first synced by [[Readwise]] [[Feb 21st, 2023]]
	- First, one must perform perfectly. The computer resembles the magic of legend in this respect, too. If one character, one pause, of the incantation is not strictly in proper form, the magic doesn't work. Human beings are not accustomed to being perfect, and few areas of human activity demand it. Adjusting to the requirement for perfection is, I think, the most difficult part of learning to program. Next, other people set one's objectives, provide one's resources, and furnish one's information. **One rarely controls the circumstances of his work, or even its goal. In management terms, one's authority is not sufficient for his responsibility. It seems that in all fields, however, the jobs where things get done never have formal authority commensurate with responsibility. In practice, actual (as opposed to formal) authority is acquired from the very momentum of accomplishment. The dependence upon others has a particular case that is especially painful for the system programmer. He depends upon other people's programs. These are often maldesigned, poorly implemented, incompletely delivered (no source code or test cases), and poorly documented. So he must spend hours studying and fixing things that in an ideal world would be complete, available, and usable. The next woe is that designing grand concepts is fun; finding nitty little bugs is just work. With any creative activity come dreary hours of tedious, painstaking labor, and programming is no exception.** ([View Highlight](https://read.readwise.io/read/01gsrdxgxhsggcaspamdxdvp51))
		- **Note**: When you are a programmer, you have to be perfect. This means that if one part of your code is wrong, the whole thing won't work. People who write code don't usually get to decide what their goals are or how their work should be done. Even though they are responsible for their work, they might not have enough power to get things done. This is true for many types of work. The hardest part for a programmer is when they have to use someone else's code. The code might be wrong, not finished, or not explained very well. Sometimes it can be fun to create big projects, but finding the small mistakes can be boring.
	- **More software projects have gone awry for lack of calendar time than for all other causes combined. Why is this cause of disaster so common? First, our techniques of estimating are poorly developed. More seriously, they reflect an unvoiced assumption which is quite untrue, i.e., that all will go well. Second, our estimating techniques fallaciously confuse effort with progress, hiding the assumption that men and months are interchangeable.**
	  
	  1.  *Key point - men and months are not interchangeable, but we make assumptions that they are* ([View Highlight](https://read.readwise.io/read/01gsreagnb45g5rd589kpz7ckb))
		- **Note**: This text points out that calendar time is the main cause of software project failure and that this is mainly due to poor estimating techniques which mistakenly assume that men and months are interchangeable. It highlights the need to recognize that men and months are not interchangeable in order to avoid project failure.
	- The dilemma is a cruel one. For efficiency and conceptual integrity, one prefers a few good minds doing design and construction. Yet for large systems one wants a way to bring considerable manpower to bear, so that the product can make a timely appearance. How can these two needs be reconciled? Mills's Proposal A proposal by Harlan Mills offers a fresh and creative solution. Mills proposes that each segment of a large job be tackled by a team, but that the team be organized like a surgical team rather than a hog-butchering team. That is, instead of each member cutting away on the problem, one does the cutting and the others give him every support that will enhance his effectiveness and productivity. ([View Highlight](https://read.readwise.io/read/01gsrdypenn3nrb2trmt644yqc))
		- **Note**: The problem is difficult. It is best to have a few smart people do the design and building of a big project. But for a big project, you need lots of people to help so it can be done quickly. How can we have both? Harlan Mills found a solution. He said the team should be like a surgical team, where one person does the cutting and the other people help that person be really good at their job.
	- Not trivial, however, is the principle that such mini-decisions be made consistently throughout. ([View Highlight](https://read.readwise.io/read/01gsrdzn6a2brmcptcrphmnbz2))
	- Fostering a total-system, user-oriented attitude may well be the most important function of the programming manager. ([View Highlight](https://read.readwise.io/read/01gsre02d20mjkp3cd71yq3wc0))
	- A good workman is known by his tools. —PROVERB ([View Highlight](https://read.readwise.io/read/01gsre13sn8eyvhcd46fztwmd2))
	- Many poor systems come from an attempt to salvage a bad basic design and patch it with all kinds of cosmetic relief. Top-down design reduces the temptation. I am persuaded that top-down design is the most important new programming formalization of the decade. ([View Highlight](https://read.readwise.io/read/01gsre9vd38e92skjqe6rtrnfk))
	- **How does one control a big project on a tight schedule? The first step is to have a schedule. Each of a list of events, called milestones, has a date. Picking the dates is an estimating problem, discussed already and crucially dependent on experience. For picking the milestones there is only one relevant rule. Milestones must be concrete, specific, measurable events, defined with knife-edge sharpness.** **It is more important that milestones be sharp-edged and unambiguous than that they be easily verifiable by the boss. Rarely will a man lie about milestone progress, if the milestone is so sharp that he can't deceive himself. But if the milestone is fuzzy, the boss often understands a different report from that which the man gives.** Sharp milestones are in fact a service to the team, and one they can properly expect from a manager. The fuzzy milestone is the harder burden to live with. It is in fact a millstone that grinds down morale, for it deceives one about lost time until it is irremediable. And chronic schedule slippage is a morale-killer. ([View Highlight](https://read.readwise.io/read/01gsre180xz071s94cazgry42n))
		- **Note**: The first step in controlling a big project on a tight schedule is to make a list of events, called milestones. Each milestone needs to have a date. It is important that the milestones are clear and specific, and not too hard for the boss to understand. This is because when the milestones are easy to understand, it is harder for people to lie about their progress. Sharp milestones are helpful to the team because they help people understand how much time they have and how much progress they are making. If the milestones are not clear and specific, it can lead to confusion and feelings of discouragement.
	- Most of the big last gains in software productivity have come from removing artificial barriers that have made the accidental tasks inordinately hard, such as severe hardware constraints, awkward programming languages, lack of machine time. How much of what software engineers now do is still devoted to the accidental, as opposed to the essential? **Unless it is more than 9/10 of all effort, shrinking all the accidental activities to zero time will not give an order of magnitude improvement. Therefore it appears that the time has come to address the essential parts of the software task, those concerned with fashioning abstract conceptual structures of great complexity. I suggest**:
	  
	  1.  Exploiting the mass market to avoid constructing what can be bought.
	  2.  Using rapid prototyping as part of a planned iteration in establishing software requirements.
	  3.  Growing software organically, adding more and more function to systems as they are run, used, and tested.
	  4.  Identifying and developing the great conceptual designers of the rising generation. ([View Highlight](https://read.readwise.io/read/01gsre2wg9rckdvn3jchdztgx9))
		- **Note**: The author suggests four steps to address the essential parts of the software task: exploiting the mass market to avoid constructing what can be bought, using rapid prototyping as part of a planned iteration in establishing software requirements, growing software organically, and identifying and developing the great conceptual designers of the rising generation. This is suggested in order to improve software productivity by focusing on the essential components of the task, rather than the accidental.
	- **Incremental development—grow, not build, software. I still remember the jolt I felt in 1958 when I first heard a friend talk about building a program, as opposed to writing one. In a flash he broadened my whole view of the software process. The metaphor shift was powerful, and accurate. Today we understand how like other building processes the construction of software is, and we freely use other elements of the metaphor, such as specifications, assembly of components, and scaffolding. The building metaphor has outlived its usefulness. It is time to change again. If, as I believe, the conceptual structures we construct today are too complicated to be accurately specified in advance, and too complex to be built faultlessly, then we must take a radically different approach. Let us turn to nature and study complexity in living things, instead of just the dead works of man. Here we find constructs whose complexities thrill us with awe. The brain alone is intricate beyond mapping, powerful beyond imitation, rich in diversity, self-protecting, and self-renewing. The secret is that it is grown, not built.** So it must be with our software systems. Some years ago Harlan Mills proposed that any software system should be grown by incremental development. That is, the system should first be made to run, even though it does nothing useful except call the proper set of dummy subprograms. Then, bit by bit it is fleshed out, with the subprograms in turn being developed into actions or calls to empty stubs in the level below. I have seen the most dramatic results since I began urging this technique on the project builders in my software engineering laboratory class. Nothing in the past decade has so radically changed my own practice, or its effectiveness. The approach necessitates top-down design, for it is a top-down growing of the software. It allows easy backtracking. It lends itself to early prototypes. Each added function and new provision for more complex data or circumstances grows organically out of what is already there. The morale effects are startling. Enthusiasm jumps when there is a running system, even a simple one. Efforts redouble when the first picture from a new graphics software system appears on the screen, even if it is only a rectangle. One always has, at every stage in the process, a working system. I find that teams can *grow* much more complex entities in four months than they can *build.* The same benefits can be realized on large projects as on my small ones. ([View Highlight](https://read.readwise.io/read/01gsre4m2y6g1kzq6g7vgyjhj5))
		- **Note**: The author suggests that software development should no longer be seen as a building process, but rather as a growing process similar to the complexity found in living things. This approach is called incremental development, and involves growing the system from the top-down, allowing for easy backtracking and early prototypes. This method has the benefit of allowing the system to be made to run quickly, and the associated morale effects are said to be "startling". It is suggested that this method allows for more complex systems to be built in a shorter period of time.
	- The differences are not minor—it is rather like Salieri and Mozart. Study after study shows that the very best designers produce structures that are faster, smaller, simpler, cleaner, and produced with less effort. The differences between the great and the average approach an order of magnitude. ([View Highlight](https://read.readwise.io/read/01gsre95kb6kjgafrmn1cx79z2))
	- **My first proposal is that each software organization must determine and proclaim that great designers are as important to its success as great managers are, and that they can be expected to be similarly nurtured and rewarded. Not only salary, but the perquisites of recognition**—office size, furnishings, personal technical equipment, travel funds, staff support—must be fully equivalent. How to grow great designers? Space does not permit a lengthy discussion, but some steps are obvious:
	  
	  1.  Systematically identify top designers as early as possible. The best are often not the most experienced.
	  2.  Assign a career mentor to be responsible for the development of the prospect, and keep a careful career file.
	  3.  Devise and maintain a career development plan for each prospect, including carefully selected apprenticeships with top designers, episodes of advanced formal education, and short courses, all interspersed with solo design and technical leadership assignments.
	  4.  Provide opportunities for growing designers to interact with and stimulate each other. ([View Highlight](https://read.readwise.io/read/01gsre5qjtdh501pbrzzdmz9y5))
		- **Note**: This text argues that software organizations should value great designers as much as great managers and reward them accordingly. It suggests four steps to cultivate great designers: identifying talent early, assigning mentors and keeping career files, creating career development plans, and providing social opportunities for them to interact with and stimulate each other.
	- Turski and I both insist that pipe-dreaming inhibits forward progress and wastes effort. ([View Highlight](https://read.readwise.io/read/01gsre8rbq7m9dr8dzs4q5yt56))
	- Representation is the essence of programming. ([View Highlight](https://read.readwise.io/read/01gsre6gbv3qp3qk5t51kjv5s2))
	- Fixing a defect has a substantial (20 to 50 percent) chance of introducing another. ([View Highlight](https://read.readwise.io/read/01gsre6p4jkjjgnqpka8sgwtkv))
	- **If one believes, as I have argued at many places in this book, that creativity comes from individuals and not from structures or processes, then a central question facing the software manager is how to design structure and process so as to enhance, rather than inhibit, creativity and initiative**. Fortunately, this problem is not peculiar to software organizations, and great thinkers have worked on it. E. F. Schumacher, in his classic, Small is Beautiful: Economics as if People Mattered, proposes a theory of organizing enterprises to maximize the creativity and joy of the workers. For his first principle he chooses the "Principle of Subsidiary Function" from the Encyclical Quadragesimo Anno of Pope Pius XI: It is an injustice and at the same time a grave evil and disturbance of right order to assign to a greater and higher association what lesser and subordinate organizations can do. For every social activity ought of its very nature to furnish help to the members of the body social and never destroy and absorb them. . . . Those in command should be sure that the more perfectly a graduated order is preserved among the various associations, in observing the principle of subsidiary function, the stronger will be the social authority and effectiveness and the happier and more prosperous the condition of the State. ([View Highlight](https://read.readwise.io/read/01gsre73kea8darhxed31zx69a))
		- **Note**: This text discusses how to design structures and processes to maximize creativity and initiative in software organizations. It cites E.F. Schumacher's book "Small is Beautiful: Economics as if People Mattered" which proposes a theory of organizing enterprises to maximize the creativity and joy of workers. It also references the "Principle of Subsidiary Function" from the Encyclical Quadragesimo Anno of Pope Pius XI which states that it is wrong to assign tasks to higher organizations when they can be done by lower organizations. The text suggests that if a graduated order is preserved among organizations and the principle of subsidiary function is observed, it will lead to stronger social authority and a happier and more prosperous state.