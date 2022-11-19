title:: "Probability Is the Logi... (highlights)
author:: [[@TivadarDanka on Twitter]]
full-title:: ""Probability Is the Logi..."
category:: #tweets
url:: https://twitter.com/TivadarDanka/status/1581228651772727296

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- "Probability is the logic of science."
	  
	  There is a deep truth behind this conventional wisdom: probability is the mathematical extension of logic, augmenting our reasoning toolkit with the concept of uncertainty.
	  
	  In-depth exploration of probabilistic thinking incoming. 
	  
	  ![](https://pbs.twimg.com/media/FfGnE9bVQAExLCs.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1581228651772727296))
		- **Note**: Thread
	- Our journey ahead has three stops:
	  
	  1. an introduction to mathematical logic,
	  2. a touch of elementary set theory,
	  3. and finally, understanding probabilistic thinking.
	  
	  First things first: mathematical logic. ([View Tweet](https://twitter.com/TivadarDanka/status/1581228654956199937))
	- In logic, we work with propositions.
	  
	  A proposition is a statement that is either true or false, like
	  
	  • "it's raining outside",
	  • "the sidewalk is wet".
	  
	  These are often abbreviated as variables, such as A = "it's raining outside". ([View Tweet](https://twitter.com/TivadarDanka/status/1581228657556672512))
	- We can formulate complex propositions from smaller building blocks with logical connectives.
	  
	  Consider the proposition "if it is raining outside, then the sidewalk is wet". This is the combination of two propositions, connected by the implication connective. ([View Tweet](https://twitter.com/TivadarDanka/status/1581228660056465408))
	- There are four essential connectives:
	  
	  • NOT (¬), also known as negation,
	  • AND (∧), also known as conjunction,
	  • OR (∨), also known as disjunction,
	  • THEN (→), also known as implication. ([View Tweet](https://twitter.com/TivadarDanka/status/1581228662501744642))
	- Connectives are defined by the truth values of the resulting propositions. For instance, if A is true, then NOT A is false; if A is false, then NOT A is true.
	  
	  Denoting true by 1 and false by 0, we can describe connectives with truth tables. Here is the one for negation (¬). 
	  
	  ![](https://pbs.twimg.com/media/FfGnF5CVQAAOj2a.png) ([View Tweet](https://twitter.com/TivadarDanka/status/1581228668482818050))
	- AND (∧) and OR (∨) connect two propositions. A ∧ B is true if both A and B are true, and A ∨ B is true if either one is. 
	  
	  ![](https://pbs.twimg.com/media/FfGnGRdVsAA97Km.png) ([View Tweet](https://twitter.com/TivadarDanka/status/1581228675059490816))
	- The implication connective THEN (→) formalizes the deduction of a conclusion B from a premise A.
	  
	  By definition, A → B is true if B is true or both A and B are false.
	  
	  An example: if "it's raining outside", THEN "the sidewalk is wet". 
	  
	  ![](https://pbs.twimg.com/media/FfGnGp8UcAAbPCj.png) ([View Tweet](https://twitter.com/TivadarDanka/status/1581228681732636672))
	- Science is just the collection of complex propositions like "if X is a closed system, THEN the entropy of X cannot decrease". (As the 2nd law of thermodynamics states.)
	  
	  The entire body of scientific knowledge is made of A → B propositions. ([View Tweet](https://twitter.com/TivadarDanka/status/1581228684920250369))
	- In practice, our thinking process is the following.
	  
	  "I know that A → B is true and A is true. Therefore, B must be true as well."
	  
	  This is called modus ponens, the cornerstone of scientific reasoning. 
	  
	  ![](https://pbs.twimg.com/media/FfGnHMKUcAE2TrV.png) ([View Tweet](https://twitter.com/TivadarDanka/status/1581228691119517696))
	- (If you don't understand modus ponens, take a look at the truth table of the → connective, a few tweets above.
	  
	  The case when A → B is true and A is true is described by the very first row, which can only happen if B is true as well.) ([View Tweet](https://twitter.com/TivadarDanka/status/1581228694302957568))
	- Logical connectives can be translated to the language of sets.
	  
	  Union (∪) and intersection (∩), two fundamental operations, are particularly relevant for us.
	  
	  Notice how similar the symbols for AND (∧) and intersection (∩) are? This is not an accident. 
	  
	  ![](https://pbs.twimg.com/media/FfGnHvQUUAU_s9u.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1581228700497895424))
	- By definition, any element 𝑥 is the element of A ∩ B if and only if (𝑥 is an element of A) AND (𝑥 is an element of B).
	  
	  Similarly, union corresponds to the OR connective. 
	  
	  ![](https://pbs.twimg.com/media/FfGnIH0VsAAYTBQ.png) ([View Tweet](https://twitter.com/TivadarDanka/status/1581228706755813377))
	- What's most important for us is that the implication connective THEN (→) corresponds to the "subset of" relation, denoted by the ⊆ symbol. 
	  
	  ![](https://pbs.twimg.com/media/FfGnIf1VIAEQpjm.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1581228713382797312))
	- Now that we understand how to formulate scientific truths as "premise → conclusion" statements and see how this translates to sets, we are finally ready to talk about probability.
	  
	  What is the biggest flaw of mathematical logic? ([View Tweet](https://twitter.com/TivadarDanka/status/1581228716440449025))
	- We rarely have all the information to decide if a proposition is true or false.
	  
	  Consider the following: "it'll rain tomorrow". During the rainy season, all we can say is that rain is more likely, but tomorrow can be sunny as well. ([View Tweet](https://twitter.com/TivadarDanka/status/1581228718965460992))
	- Probability theory generalizes classical logic by measuring truth on a scale between 0 and 1, where 0 is false and 1 is true.
	  
	  If the probability of rain tomorrow is 0.9, it means that rain is significantly more likely, but not absolutely certain. ([View Tweet](https://twitter.com/TivadarDanka/status/1581228721498779649))
	- Instead of propositions, probability operates on events. In turn, events are represented by sets.
	  
	  For example, if I roll a dice, the event "the result is less than five" is represented by the set A = {1, 2, 3, 4}.
	  
	  In fact, P(A) = 4/6. (P denotes the probability of an event.) ([View Tweet](https://twitter.com/TivadarDanka/status/1581228724090851328))
	- As discussed earlier, the logical connectives AND and OR correspond to basic set operations: AND is intersection, OR is union.
	  
	  This translates to probabilities as well. 
	  
	  ![](https://pbs.twimg.com/media/FfGnJe_VEAAItKi.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1581228730873020417))
	- How can probability be used to generalize the logical implication?
	  
	  A "probabilistic A → B" should represent the likelihood of B, given that A is observed.
	  
	  This is formalized by conditional probability. 
	  
	  ![](https://pbs.twimg.com/media/FfGnJ6RUUAAPB0F.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1581228737969823744))
	- (If you want to know more about conditional probabilities, here is a brief explainer.)
	  
	  https://t.co/FgioyJN8xj ([View Tweet](https://twitter.com/TivadarDanka/status/1581228741027540992))
	- At the deepest level, the conditional probability P(B | A) is the mathematical formulation of our belief in the hypothesis B, given empirical evidence A.
	  
	  A high P(B | A) makes B more likely to happen, given that A is observed. 
	  
	  ![](https://pbs.twimg.com/media/FfGnKeYVsAAKwMt.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1581228747553808384))
	- On the other hand, a low P(B | A) makes B less likely to happen when A occurs as well.
	  
	  This is why probability is called the logic of science. 
	  
	  ![](https://pbs.twimg.com/media/FfGnK37UYAExROC.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1581228754688303104))
	- To give you a concrete example, let's go back to the one mentioned earlier: the rain and the wet sidewalk. For simplicity, denote the events by
	  
	  A = "the sidewalk is wet",
	  B = "it's raining outside". ([View Tweet](https://twitter.com/TivadarDanka/status/1581228757745967104))
	- The sidewalk can be wet for many reasons, say the neighbor just watered the lawn. Yet, the primary cause of a wet sidewalk is rain, so P(B | A) is close to 1.
	  
	  If somebody comes in and tells you that the sidewalk is wet, it is safe to infer rain. ([View Tweet](https://twitter.com/TivadarDanka/status/1581228760262508546))
	- Probabilistic inference like the above is the foundation of machine learning.
	  
	  For instance, the output of (most) classification models is the distribution of class probabilities, given an observation. 
	  
	  ![](https://pbs.twimg.com/media/FfGnLlDVUAAWYWb.jpg) ([View Tweet](https://twitter.com/TivadarDanka/status/1581228766696964096))
	- To wrap up, here is how Maxwell — the famous physicist — thinks about probability.
	  
	  "The actual science of logic is conversant at present only with things either certain, impossible, or entirely doubtful, none of which (fortunately) we have to reason on." ([View Tweet](https://twitter.com/TivadarDanka/status/1581228769787883520))
	- "Therefore the true logic for this world is the calculus of Probabilities, which takes account of the magnitude of the probability which is, or ought to be, in a reasonable man's mind."
	  
	  (James Clerk Maxwell)
	  
	  By now, you can fully understand what Maxwell meant. ([View Tweet](https://twitter.com/TivadarDanka/status/1581228772291801088))
	- Read the unrolled thread here:
	  
	  https://t.co/2XQqCBkSAo ([View Tweet](https://twitter.com/TivadarDanka/status/1581228774833541121))
	- If you have enjoyed this thread, share it with your friends and follow me!
	  
	  I regularly post deep-dive explanations about mathematics and machine learning. https://t.co/bGdyx0LAjP ([View Tweet](https://twitter.com/TivadarDanka/status/1581228777396350976))