title:: You Can Switch From Sums... (highlights)
author:: [[@johncarlosbaez on Twitter]]
full-title:: "You Can Switch From Sums..."
category:: #tweets
url:: https://twitter.com/johncarlosbaez/status/1567108092856344576

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- You can switch from sums to integrals in the definition of entropy, but be careful - a bunch of things change!  
	  
	  When you switch to integrals, the entropy can be negative, it can be infinite - and most importantly, it depends on your choice of coordinates.
	  
	  (1/n) 
	  
	  ![](https://pbs.twimg.com/media/Fb98CAlXgAA2uwc.jpg) ([View Tweet](https://twitter.com/johncarlosbaez/status/1567108092856344576))
		- **Note**: Thread
	- We run into this with any classical system that obeys the equipartition theorem, like a classical harmonic oscillator or ideal gas.  Its entropy becomes negative at low temperatures!   
	  
	  So, it doesn't obey the Third Law.   That's the way out of this "paradox".
	  
	  (2/n) 
	  
	  ![](https://pbs.twimg.com/media/Fb9-HcLWQAEG5Mf.jpg) ([View Tweet](https://twitter.com/johncarlosbaez/status/1567110253539360769))
		- **Tags**: #[[thermodynamics]]
	- Say a classical system has Rⁿ as its space of states.  If it has a single state of least energy, as T → 0 the Gibbs distribution typically approaches a delta function sitting at this state.  And as this happens, 
	  
	  S(p) = -∫p(x) ln p(x) dⁿx  
	  
	  becomes negative! 
	  
	  (3/n) ([View Tweet](https://twitter.com/johncarlosbaez/status/1567112111125397509))
	- Worse, the entropy changes under coordinate transformations that don't preserve the measure dⁿx.   So, you need some physical argument to justify the coordinates you use to compute entropy - or more precisely, the measure you're using.   I should explain how this works.
	  
	  (4/n) ([View Tweet](https://twitter.com/johncarlosbaez/status/1567113467613663235))
	- The entropy 
	  
	  S(p) = -∫p(x) ln p(x) dⁿx  
	  
	  can also become +∞ when the probability distribution p(x) is really spread out.   But in practice this doesn't happen as often the other two problems.   I just had to admit it: I'm a mathematician, after all.
	  
	  (5/n) ([View Tweet](https://twitter.com/johncarlosbaez/status/1567114153701085184))
	- The real point: integrals become sums when we use 'counting measure', where each point in a set has measure 1.   Counting measure is invariant under all permutations, and entropy computed using counting measure is always ≥ 0, though it can be +∞ if the set is infinite.
	  
	  (6/n) ([View Tweet](https://twitter.com/johncarlosbaez/status/1567114985301590017))
	- But when computing entropy in classical mechanics, we often use a measure other than counting measure.   Then we need to work harder to justify using this measure!
	  
	  For R² with one position coordinate q and one momentum coordinate p, the right measure is
	  
	  dp dq / ℏ
	  
	  (7/n) ([View Tweet](https://twitter.com/johncarlosbaez/status/1567116310030557185))
	- dp dq is called the 'Liouville measure'.   Any multiple of it is preserved by time evolution according to Hamilton's equations.  But it has units of action!  We must divide it by something with units of action to get the units right on entropy.
	  
	  (8/n)
	  https://t.co/3b7rnfmUKV ([View Tweet](https://twitter.com/johncarlosbaez/status/1567117420204068864))
	- Conveniently, Planck's constant ℏ has units of action!  So 
	  
	  dp dq / ℏ
	  
	  is a good measure on R² to define entropy for a classical system with one position variable and one momentum variable.  
	  
	  But that's weird: Planck's constant in classical statistical mechanics! 🤔
	  
	  (9/n) ([View Tweet](https://twitter.com/johncarlosbaez/status/1567118626905260032))
	- It's weird but true.   It hints at the secret unity of statistical mechanics and quantum mechanics.
	  
	  Classical statistical mechanics doesn't work well without at least a tiny bit of quantum theory!
	  
	  That's how quantum theory was discovered in the first place.
	  
	  (10/n, n = 10) ([View Tweet](https://twitter.com/johncarlosbaez/status/1567119261679640576))