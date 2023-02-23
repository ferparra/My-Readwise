title:: ML Beyond Curve Fitting: An Intro to Causal Inference and Do-Calculus (highlights)
author:: [[inference.vc]]
full-title:: "ML Beyond Curve Fitting: An Intro to Causal Inference and Do-Calculus"
category:: #articles
url:: https://www.inference.vc/untitled/

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- Pearl dismisses most of what we do in ML as curve fitting
	- Calling machine learning alchemy was a great recent example
	- highlighting causal inference as a huge, relatively underexplored, application of deep learning
	- causal calculus differentiates between two types of conditional distributions one might want to estimate
	- observational p(y|x)p(y|x)p(y\vert x): What is the distribution of YYY given that I observe variable XXX takes value xxx. This is what we usually estimate in supervised machine learning. It is a conditional distribution which can be calculated from p(x,y,z,…)p(x,y,z,…)p(x,y,z,\ldots) as a ratio of two of its marginals. p(y|x)=p(x,y)p(x)p(y|x)=p(x,y)p(x)p(y\vert x) = \frac{p(x,y)}{p(x)}. We're all very familiar with this object and also know how to estimate this from data.
	- interventional p(y|do(x))p(y|do(x))p(y\vert do(x)): What is the distribution of YYY if I were to set the value of XXX to xxx. This describes the distribution of YYY I would observe if I intervened in the data generating process by artificially forcing the variable XXX to take value xxx, but otherwise simulating the rest of the variables according to the original process that generated the data. (note that the data generating procedure is NOT the same as the joint distribution p(x,y,z,…)p(x,y,z,…)p(x,y,z,\ldots) and this is an important detail).
	- yyy and xxx are correlated or statistically dependent and therefore seeing xxx allows me to predict the value of yyy, but yyy is not caused by xxx so setting the value of xxx won't effect the distribution of yyy
	- p(y|x)p(y|x)p(y\vert x) and p(y|do(x))p(y|do(x))p(y\vert do(x)) behave very differently
	- seek to estimate one of these conditionals
	- In applications where you ultimately want to control or choose xxx based on the conditional you estimated, you should seek to estimate p(y|do(x))p(y|do(x))p(y\vert do(x)) instead
	- proactively choose the treatment xxx given our understanding of how it effects the outcome yyy
	- system identification, control and online recommender systems
	- p(y|do(x))p(y|do(x))p(y\vert do(x)) is in fact a vanilla conditional distribution, but it's not computed based on p(x,z,y,…)p(x,z,y,…)p(x,z,y,\ldots), but a different joint pdo(X=x)(x,z,y,…)pdo(X=x)(x,z,y,…)p_{do(X=x)}(x,z,y,\ldots) instead. This pdo(X=x)pdo(X=x)p_{do(X=x)} is the joint distribution of data which we would observe if we actually carried out the intervention in question
	- p(y|do(x))p(y|do(x))p(y\vert do(x)) is the conditional distribution we would learn from data collected in randomized controlled trials or A/B tests where the experimenter controls xxx.
	- If I cannot measure p(y|do(x))p(y|do(x))p(y\vert do(x)) directly in a randomized controlled trial, can I estimate it based on data I observed outside of a controlled experiment?
	- The only way we can make predictions about how our distribution changes as a consequence of an interaction is if we know how the variables are causally related
	- Once we have a causal diagram, we can emulate the effect of intervention by mutilating the causal network: deleting all edges that lead into nodes in a dododo operator
	- as a result of a do-calculus derivation you end up with an equivalent formula for p̃ (y|do(x))p~(y|do(x))\tilde{p}(y\vert do(x)) which no longer has any do operators in them, so you estimate it from observational data alone
	- a full causal model is a form of prior knowledge that you have to add to your analysis in order to get answers to causal questions without actually carrying out intervention
	- It allows us to answer "what-if-we-did-x" type questions that would normally require controlled experiments and explicit interventions to answe
	- [[Causal inference]] and [[do-calculus]] allows you to understand a problem and establish what needs to be estimated from data based on your assumptions captured in a causal diagram