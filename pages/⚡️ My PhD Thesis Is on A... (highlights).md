title:: ⚡️ My PhD Thesis Is on A... (highlights)
author:: [[@PatrickKidger on Twitter]]
full-title:: "⚡️ My PhD Thesis Is on A..."
category:: #tweets
url:: https://twitter.com/PatrickKidger/status/1491069456185200640

- Highlights first synced by [[Readwise]] [[Dec 18th, 2022]]
	- ⚡️ My PhD thesis is on arXiv! ⚡️
	  
	  To quote my examiners it is "the textbook of neural differential equations" - across ordinary/controlled/stochastic diffeqs.
	  
	  w/ unpublished material:
		- **Note**: Thread
	- If you follow me then there's a decent chance that you already know what an NDE is. (If you don't, go read the introductory Chapter 1 to my thesis haha -- it's only 6 pages long.) Put a neural network inside a differential equation, and suddenly cool stuff starts happening.
	  
	  2/n 
	  
	  ![](https://pbs.twimg.com/media/FLFTF-uXwAA3vAg.jpg) ([View Tweet](https://twitter.com/PatrickKidger/status/1491069461637791748))
	- Neural differential equations are a beautiful way of building models, offering:
	- You can model the evolution of unknown trajectories (cough finance cough) via neural SDEs:
	  
	  4/n 
	  
	  ![](https://pbs.twimg.com/media/FLFTCFHWUAEMNHC.jpg) ([View Tweet](https://twitter.com/PatrickKidger/status/1491069468935860224))
	- ...or model unknown distributions via continuous normalising flows (aka the Fokker--Planck equation):
	  
	  In this case the target distribution is a 2D picture. (Obtained by me and Microsoft Paint at 2am.)
	  
	  5/n 
	  
	  ![](https://pbs.twimg.com/media/FLFTPCjXIAIUf1X.jpg) ([View Tweet](https://twitter.com/PatrickKidger/status/1491069474157785092))
	- Or you can study unknown physical dynamics -- here an unknown Hamiltonian system parameterised by neural kinetic and potential terms:
	  
	  6/n 
	  
	  ![](https://pbs.twimg.com/media/FLFS4OFXwAQixGY.jpg) ([View Tweet](https://twitter.com/PatrickKidger/status/1491069479463559171))
	- You can build "continuous time RNNs", by using the theory of controlled differential equations:
	  
	  7/n 
	  
	  ![](https://pbs.twimg.com/media/FLFTlXEXMAETdXa.jpg) ([View Tweet](https://twitter.com/PatrickKidger/status/1491069485121429508))
	- As a final example, you can understand neural nets via diffeqs. It's relatively famous that ResNets are the explicit Euler method applied to a neural ODE...
	  
	  8/n 
	  
	  ![](https://pbs.twimg.com/media/FLFTvyJWUAwZzFU.jpg) ([View Tweet](https://twitter.com/PatrickKidger/status/1491069490461036545))
	- ...but did you know that the feature that distinguishes GRUs and LSTMs from generic RNNs, is a very precise differential-equation-like structure? For example a GRU has an exponential decay term.
	  
	  (No wonder they struggle to learn long-term dependencies.)
	  
	  9/n 
	  
	  ![](https://pbs.twimg.com/media/FLFUCtFXsAEK2_P.jpg) ([View Tweet](https://twitter.com/PatrickKidger/status/1491069495431286789))
	- I've hinted that my thesis includes some previously unpublished material.
	  
	  For example, did you know that a neural ODE can be a universal approximator even if its vector fields are not universal approximators? (That's Section 2.4.2.)
	  
	  10/n 
	  
	  ![](https://pbs.twimg.com/media/FLFUlsGXIAAHQtj.jpg) ([View Tweet](https://twitter.com/PatrickKidger/status/1491069500854317060))
	- Or that all these "adjoint methods" floating about
	- If you've ever heard of SINDy -- symbolic regression for dynamical systems -- then there's *also* some unpublished material on improving on this via genetic algorithms. (That's Section 6.1.)
	  
	  [@MilesCranmer who this was joint work with!]
	  
	  12/n 
	  
	  ![](https://pbs.twimg.com/media/FLFVPYBWQAca_vF.jpg) ([View Tweet](https://twitter.com/PatrickKidger/status/1491069510895702022))
	- And of course, all accompanying code is provided -- available as the examples in the brand-new Diffrax software library! Your one-stop-shop for numerical differential equation solvers in #JAX.
	  
	  GitHub: https://t.co/6zSV2BeASW
	  Documentation: https://t.co/ypdkWT0yt7
	  
	  13/n ([View Tweet](https://twitter.com/PatrickKidger/status/1491069513588264961))
	- I'm planning on doing some individual posts about some highlights from the thesis over the next few days.
	  
	  Diffrax is available a little early as a sneak peak. I'll be doing a proper announcement on it next week!
	  
	  14/n 
	  
	  ![](https://pbs.twimg.com/media/FLFVphXXwAE1D4f.jpg) ([View Tweet](https://twitter.com/PatrickKidger/status/1491069518642581505))
	- Credit where it's due. A doctorate doesn't happen in a vacuum.
	  
	  My friends and friends have been an amazing support. Chloe, thank you for all the food! Juliette, thank you for the south of France. Mum, Dad: thank you for everything.
	  
	  On a more academic note:
	  
	  15/n ([View Tweet](https://twitter.com/PatrickKidger/status/1491069521482104837))
	- (Feel free to @ everyone else who'd like to know about this!)
	  
	  I have been fortunate to work, collaborate, or communicate with most of the above list. (+Many others, both on and off Twitter.) So in a very practical way, you made this work possible.
	  
	  17/n ([View Tweet](https://twitter.com/PatrickKidger/status/1491069525517037568))
	- Okay, let's wrap this up. If you're studying NDEs and want a reference text, then maybe this is it?
	  
	  231 pages of everything you ever wanted to know about N ordinary DEs, N controlled DEs, N stochastic DEs, and N rough DEs.
	  
	  Once again, link here: https://t.co/Pm5l6FhEED
	  
	  18/18 ([View Tweet](https://twitter.com/PatrickKidger/status/1491069527589031941))
	- Appendix: as a fun historical note, whilst "Neural Ordinary Differential Equations" won best paper at NeurIPS 2018 -- which is why people have heard of the field of NDEs -- I'm actually aware of work on NDEs dating back to 1991!
	  
	  https://t.co/ZUYwD2N9ep
	  
	  19/18 ([View Tweet](https://twitter.com/PatrickKidger/status/1491069529635827713))
	- Also, do check out the "Comments" section at the end of each chapter. There you can find various marginalia on extensions, references, open problems, and musings about the field of NDEs in general. :)
	  
	  20/18
	  
	  Fin. [Both of this tweet thread... and of my doctorate!] https://t.co/W96gbvzRls ([View Tweet](https://twitter.com/PatrickKidger/status/1491069538812973061))
	- @Farakay41 That caution given, there are definitely possibilities for "neural Navier Stokes". For example modelling closure relations (e.g. in turbulence). That's a term without a theoretical derivation, so a data-driven approach becomes your main choice. (Section 2.2.2.1; "use cases")
	  
	  2/3 ([View Tweet](https://twitter.com/PatrickKidger/status/1491342433493614595))
	- @Farakay41 For general PDEs, this is almost completely wide open. CNNs and PDEs have obvious connections, and there is work on Fourier Neural Operator and Neural SPDEs, but the ideas here are still nascent. I'd describe this as one of the major open diretions for NDEs. (Chapter 7)
	  
	  3/3 ([View Tweet](https://twitter.com/PatrickKidger/status/1491342465835495426))
	- @AdrienCorenflos Incidentally, the "Scalable..." paper did learn the diffusion as well. (It just happened to be shared between two SDEs; overall they optimise two drifts and one diffusion.)
	  
	  2/2 ([View Tweet](https://twitter.com/PatrickKidger/status/1491368863136874497))
	- @AdrienCorenflos Coming back to this: sorry, I see now that the integrand of Prop 3.1 has # params as its only free index. I think I'll need to stare at this for a bit longer to figure out the intuition. It *does* still have an expensive matrix pseudoinversion; and the approach 
	  1/3 ([View Tweet](https://twitter.com/PatrickKidger/status/1491405306911346695))
	- @AdrienCorenflos we've taken generalises the ODE case, rather than being SDE-only. So I think I stand by "our version" being better. (Not that this about choosing sides!) But I think you're right - I don't think I stand by the statement about fwd-mode autodiff.
	  
	  2/3 ([View Tweet](https://twitter.com/PatrickKidger/status/1491405506958991360))
	- @AdrienCorenflos (or at least "maybe very close to zero") ([View Tweet](https://twitter.com/PatrickKidger/status/1491414985633054722))