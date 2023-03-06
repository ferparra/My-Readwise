title:: OpenAI's Leaked Foundry... (highlights)
author:: [[@labenz on Twitter]]
full-title:: "OpenAI's Leaked Foundry..."
category:: #tweets
url:: https://twitter.com/labenz/status/1630284912853917697

- Highlights first synced by [[Readwise]] [[Feb 28th, 2023]]
	- OpenAI's leaked Foundry pricing says a lot – if you know how to read it – about GPT4, The Great Implementation, a move from Generative to Productive AI, OpenAI's safety & growth strategies, and the future of work.
	  
	  Another AI-obsessive megathread on what to expect in 2023 🧵 
	  
	  ![](https://pbs.twimg.com/media/Fp_p8uWX0AMk-nW.jpg) ([View Tweet](https://twitter.com/labenz/status/1630284912853917697))
		- **Note**: Thread
	- Disclaimer: I'm an OpenAI customer, but this analysis is based purely on public info
	  
	  I asked our business contact if they could talk about Foundry, and got a polite "no comment"  
	  
	  As this is outside analysis, I'm sure I'll get some details wrong, and trust you'll let me know 🙏 ([View Tweet](https://twitter.com/labenz/status/1630284914678480913))
	- If you prefer to read this on a substack, sign up for mine right here.
	  
	  In the future I might publish something there and not here, and you wouldn't want to miss that.  :) 
	  
	  https://t.co/UB8HxcBqgm ([View Tweet](https://twitter.com/labenz/status/1630284916125495298))
	- So without further ado… what is "Foundry"?  
	  
	  Quoting the pricing sheet, it's the "platform for serving" OpenAI's "latest models", which will "soon" come with "more robust fine-tuning" options. ([View Tweet](https://twitter.com/labenz/status/1630284917648027648))
	- "Latest models" – plural – says a lot
	  
	  GPT4 is not a single model, but a class of models, defined by pre-training scale & parameter count, and perhaps some standard RLHF.
	  
	  MSFT's Prometheus is the first public GPT4-class model, and does some crazy stuff!
	  
	  https://t.co/mSuBQmrsAG ([View Tweet](https://twitter.com/labenz/status/1630284919401246721))
	- Safe to say these latest models have more pre-training than anything else we've seen, and it doesn't sound like they've hit a wall.
	  
	  https://t.co/Pgxkj7WshQ ([View Tweet](https://twitter.com/labenz/status/1630284921716584450))
	- Nevertheless, I'll personally bet that the "robust fine-tuning" will drive most of the adoption, value, and transformation in the near term. ([View Tweet](https://twitter.com/labenz/status/1630284923557773318))
	- Conceptually, an industrial foundry is where businesses make the tools that make their physical products. OpenAI's Foundry will be where businesses build AIs to perform their cognitive tasks – also known as *services*, also known as ~75% of the US economy! ([View Tweet](https://twitter.com/labenz/status/1630284924967108609))
	- The "Foundry" price range, from ~$250K/year for "3.5-Turbo" (ChatGPT scale) to $1.5M/yr for 32K context-window "DV", suggests that OpenAI can readily demonstrate GPT4's ability to do meaningful work in corporate settings in a way that inspires meaningful financial commitments ([View Tweet](https://twitter.com/labenz/status/1630284926485422083))
	- This really should not be a surprise, because ChatGPT can pass the Bar Exam, and fine-tuned models such as MedPaLM are starting to approach human professional levels as well.
	  
	  Most routine cognitive work is not considered as demanding as these tests!
	  
	  https://t.co/UEkdl573wG ([View Tweet](https://twitter.com/labenz/status/1630284927924051969))
	- The big problems with LLMs, of course, have been hallucinations, limited context windows, and inability to access up-to-date information or use tools.  We've all seen flagrant errors and other strange behaviors from ChatGPT and especially New Bing. ([View Tweet](https://twitter.com/labenz/status/1630284930126172161))
	- Keep in mind, though, that the worst failures happen in a zero-shot, open domain setting, often under adversarial conditions
	  
	  People are working increasingly hard to jailbreak and embarrass them. Considering this, it's amazing how well they do perform.
	  
	  https://t.co/16ZhUouRUk ([View Tweet](https://twitter.com/labenz/status/1630284931720007681))
	- When you know what you want an AI to do and have the opportunity to fine-tune models to do it, it's an entirely different ball game. ([View Tweet](https://twitter.com/labenz/status/1630284933678678016))
	- For the original "davinci" models (now 3 generations behind if you count Instruct, ChatGPT, and upcoming DV"), OpenAI recommends "Aim for at least ~500 examples" as a starting point for fine-tuning. 
	  
	  https://t.co/PntyoxofKW ([View Tweet](https://twitter.com/labenz/status/1630284935180197890))
	- Personally, I've found that as few as 20 examples can work for very simple tasks, which again, isn't surprising given that LLMs are few-shot learners and that there's a conceptual (near-?) equivalence between few-shot and fine-tuning approaches.  
	  
	  https://t.co/7SuHutaqXF ([View Tweet](https://twitter.com/labenz/status/1630284936845434880))
	- In any case, in corporate "big data" terms, whether you need 50 or 500 or 5000 examples, it's all tiny!  Imagine what corporations will be able to do with all those call center records they've been keeping … for, as it turns out, AI training purposes. ([View Tweet](https://twitter.com/labenz/status/1630284938980253696))
	- The new 32000-token context window is also a huge deal.  This is enough for 50 pages of text or a 2-hour conversation.  For many businesses, that's enough to contain your entire customer profile and history. ([View Tweet](https://twitter.com/labenz/status/1630284940322512896))
	- Others will need retrieval & "context management" strategies
	  
	  That's where embeddings, vector databases, and dev frameworks like @LangChainAI and @PromptableAI come in!
	  
	  Watch out for upcoming @CogRev_Podcast conversation with @trychroma founder @atroyn
	  
	  https://t.co/7AvIz4aZj5 ([View Tweet](https://twitter.com/labenz/status/1630284941677285377))
	- Aside: this pricing also suggests the possibility of an undisclosed algorithmic advance
	  
	  [[Attention mechanism]] inference costs rise with the square of the context window.  Yet, we see a 4X jump in context – which would suggest a 16X increase in cost – with just a 2X jump in price🤔 
	  
	  ![](https://pbs.twimg.com/media/Fp_tK9oX0AE5wDJ.jpg) ([View Tweet](https://twitter.com/labenz/status/1630284944508428288))
	- In any case, the combination of fine-tuning and context window expansion, especially as supported by the rapidly evolving LLM tools ecosystem, mean customers will be able to achieve human performance & reliability – or better! – on many economically valuable tasks – in 2023! ([View Tweet](https://twitter.com/labenz/status/1630284946274152449))
	- Meanwhile, image & video generation, speech generation, and speech recognition have all recently hit new highs, and there's more coming from eg @play_ht, heard here as the voice of ChatGPT.
	  
	  Mahmoud is another upcoming @CogRev_Podcast  guest!
	  
	  https://t.co/Fi5Kyo5FBu ([View Tweet](https://twitter.com/labenz/status/1630284947670925312))
	- So what might corporations train models to do in 2023?
	  
	  In short, tasks with a documented, standard operating procedure will be transformed first.  
	  
	  Work that requires original thought, sophisticated reasoning, or advanced strategy will be much less affected in the short term. ([View Tweet](https://twitter.com/labenz/status/1630284951487741958))
	- This is a bit of a reversal from how things are usually understood.  LLMs are celebrated for their ability to write creative poems in seconds, but dismissed when it comes to doing anything that matters.  
	  
	  I think that's about to change, and I'm not alone
	  
	  https://t.co/BQ5rgjNsF9 ([View Tweet](https://twitter.com/labenz/status/1630284953001885697))
	- The AI UX paradigm will shift from one that delivers a response but puts the onus on the user to evaluate and figure out what to do with it, to one where AIs are directly responsible for getting things done, and humans supervise.  
	  
	  I call this The Great Implementation ([View Tweet](https://twitter.com/labenz/status/1630284954939670528))
	- Specifically, within 2023, I expect custom models will be trained to…. ([View Tweet](https://twitter.com/labenz/status/1630284956390903816))
	- Create, re-purpose, and localize content – full brand standards fit into 32K tokens, with plenty of room to write some tweets.
	  
	  Amazingly my own company @Waymark is mentioned with  Patrón, Spectrum, Coke, and OpenAI in this article.  
	  https://t.co/di2sXLXfWB ([View Tweet](https://twitter.com/labenz/status/1630285200155353088))
	- Handle customer interactions – natural language Q&A, appointment setting, account management, and even tech support, available 24/7, pick up where you left off, text or voice.
	  
	  Customer service and experience will improve dramatically!
	  
	  https://t.co/PbzJSQ8tAT ([View Tweet](https://twitter.com/labenz/status/1630285413515419653))
	- Streamline hiring – in such a hot market, personalizing outreach, assessing resumes, summarizing & flagging profiles, suggesting interview questions.  For companies who have an overabundance of candidates, perhaps even conducting initial interviews? ([View Tweet](https://twitter.com/labenz/status/1630285471065550848))
	- Coding – with knowledge of private code bases, following your coding standards.  Copilot is just the beginning here.  
	  
	  https://t.co/DVSlSQla4w ([View Tweet](https://twitter.com/labenz/status/1630285792038862848))
	- Conduct research using a combination of public search and private retrieval.  
	  
	  See this master class, must-read thread from @jungofthewon about best-in-class @elicitorg – it really does meaningful research for you!
	  
	  https://t.co/34i9lEqMOL ([View Tweet](https://twitter.com/labenz/status/1630286063632625666))
	- Analyze data, and generate, review, summarize reports – all sorts of projects can now "talk to data" – another of the leaders is @gpt_index 
	  
	  https://t.co/K7NdpjWhGK ([View Tweet](https://twitter.com/labenz/status/1630286183027601409))
	- Execute processes by calling a mix of public and private APIs – sending emails, processing transactions, etc, etc, etc.  We're starting to see this in the research as well.
	  
	  https://t.co/qNqYSyW10Y ([View Tweet](https://twitter.com/labenz/status/1630286271527485442))
	- How will this happen in practice?  And what will the consequences be for work and jobs??
	  
	  For starters, it's less about AI doing jobs and more about AI doing tasks. ([View Tweet](https://twitter.com/labenz/status/1630286341589139458))
	- Many have argued that human jobs  require more context and physical dexterity than AIs currently have, and thus that AIs will not be able to do most jobs.
	  
	  This is true, but misses a key point, which is that the way work is organized can and will change to take advantage of AI. ([View Tweet](https://twitter.com/labenz/status/1630286439299571712))
	- What's actually going to happen is not that humans will be dropped into human roles, but that the tasks which add up to jobs will be pulled apart into discrete bits that AIs can perform. ([View Tweet](https://twitter.com/labenz/status/1630286516587986949))
	- There is precedent for such a change in the mode of production. As recently as ~100 years ago, physical manufacturing looked a lot more like modern knowledge work. Pieces fit together loosely, and people solved lots of small production problems on the fly with skilled machining ([View Tweet](https://twitter.com/labenz/status/1630286787175120897))
	- Interchangeable parts & assembly lines changed all that; standardization and tighter tolerances unlocked reliable performance at scale.  This transformation is largely complete in manufacturing – people run machines that do almost all of the work with very high precision. ([View Tweet](https://twitter.com/labenz/status/1630286863268294657))
	- Services lag manufacturing because services are mediated by language, and the art of mapping conversation onto actions is hard to standardize. Businesses try, but people struggle to consistently use best practices. Every CMO complains that people don't respect brand standards. ([View Tweet](https://twitter.com/labenz/status/1630287215837192192))
	- The Great Implementation will bring about a shift from humans doing the tasks that constitute "Services" to the humans building, running, maintaining, and updating the machines that do the tasks that constitute services. ([View Tweet](https://twitter.com/labenz/status/1630287270937755649))
	- In many cases, those will be different humans.  And this is where OpenAI's "global services alliance" with Bain comes in.
	  
	  https://t.co/qy2rCGot16 ([View Tweet](https://twitter.com/labenz/status/1630287400634130432))
	- The core competencies needed to develop and deploy fine-tuned GPT4 models in corporate settings include: ([View Tweet](https://twitter.com/labenz/status/1630287456405733378))
	- *Problem definition* – what are we trying to accomplish, and how do we structure that as a text prompt & completion?  What information do we need to include in the prompt to ensure that the AI has everything it needs to perform the task? ([View Tweet](https://twitter.com/labenz/status/1630287532914098176))
	- *Training data curation / adaptation / creation* – what constitutes a job well done?  do we have records of this?  do the records reflect implicit knowledge that the AI will need, or perhaps contain certain information (eg - PII) that should not be trained into a model at all? ([View Tweet](https://twitter.com/labenz/status/1630287673129590785))
	- *Validation, Error Handling, and Red Teaming*  – how does model performance compare to humans?  how do we detect failures, and what do we do about them?  and how can we be confident that we'll avoid New Bing type behaviors? ([View Tweet](https://twitter.com/labenz/status/1630287757250646018))
	- There is an art to all of these, but they are not super hard skills to learn.  Certainly a typical Bain consultant will be able to get pretty good at most of them.  And the same basic approach will work across many environments.  Specialization makes sense here. ([View Tweet](https://twitter.com/labenz/status/1630287846413090816))
	- Additionally, the hardest part about organizational change is often that organizations don't want to change.  With that in mind, it's no coincidence that leadership turns to consultants who are known for helping corporations manage re-organizations, change, and yes – layoffs. ([View Tweet](https://twitter.com/labenz/status/1630287978441392128))
	- Consultants have talked like this forever, but this time it's literally true.  
	  
	  Btw @BainAlerts ... may I suggest Cognitive Revolution instead of "industrial revolution for knowledge work"?   
	  
	  :) 
	  
	  ![](https://pbs.twimg.com/media/Fp_yhObXoAQwjy8.png) ([View Tweet](https://twitter.com/labenz/status/1630288405262106624))
	- So, no, AI won't take jobs, but it will do parts of jobs, and many jobs may cease to exist in their current form. There's precedent for this too, when mechanization came to agriculture
	  
	  Will the people affected will find other jobs? I don't know
	  
	  https://t.co/rFfcmXHUT8 ([View Tweet](https://twitter.com/labenz/status/1630288829675347968))
	- Finally … WHY is OpenAI going this route with pricing?  It's a big departure from the previous "API first", usage-based pricing strategy, and the technology would be no less transformative with that model.  I see 2 big reasons for this approach: (1) safety/control and (2) $$$ ([View Tweet](https://twitter.com/labenz/status/1630288971593916420))
	- re: Safety – @SamA has said OpenAI will deploy GPT4 when they are confident it's safe to do so.
	  
	  A $250K entry point suggests a "know your customer" approach to safety, likely including vetting customers, reviewing use cases, etc.  
	  
	  They did this for GPT3 and DALLE2 too. ([View Tweet](https://twitter.com/labenz/status/1630289310539808768))
	- Of course, this doesn't mean things will be entirely predictable or safe.
	  
	  I doubt that the OpenAI team that shipped ChatGPT would have signed off  on "Sydney" – my guess is that MSFT ran their own fine-tuning & QA processes.
	  
	  More here: https://t.co/9HUHEm68Xu ([View Tweet](https://twitter.com/labenz/status/1630289809552949249))
	- re: $$$ – this is a natural way for OpenAI to use access to their best models to protect their lower-end business from cheaper / open source alternatives, and to some degree discourage / crowd out in-house corporate investments in AI. ([View Tweet](https://twitter.com/labenz/status/1630289943003119621))
	- I am always going on about threshold effects, and how application developers will generally want to use the smallest/cheapest/fastest models that suffice for their use case.  
	  
	  This is already starting to happen – see @jungofthewon again
	  https://t.co/Ee5TOfFjIg ([View Tweet](https://twitter.com/labenz/status/1630290084694982656))
	- With Meta having just (sort-of) released new ~SOTA models and @StabilityAI soon to release even better, the stage is set for a lot more customers to go this way, at least as long as OpenAI has such customer-friendly, usage-based, no commitment pricing
	  
	  https://t.co/akmF1GBo4Y ([View Tweet](https://twitter.com/labenz/status/1630290695905763329))
	- OpenAI can't prevent other projects from hitting key thresholds, but they can change customer calculus.  Why chase pennies on base use cases when you've already spent big bucks on dedicated capacity?  And is there budget for an ML PhD after we just dropped $1.5M on DV 32K? ([View Tweet](https://twitter.com/labenz/status/1630291074450169859))
	- In conclusion, economically transformative AI is not only here, but OpenAI is already selling it
	  
	  We'll feel it once models are fine-tuned and integrated into existing systems
	  
	  A lot will happen in 2023, but of course The Great Implementation will go on for years
	  
	  Buckle up! ([View Tweet](https://twitter.com/labenz/status/1630291495499489285))
	- If you made it this far, I'll of course appreciate your retweets, as well as your critical commentary.
	  
	  https://t.co/FAh8DSGbnk ([View Tweet](https://twitter.com/labenz/status/1630291824932802567))
	- And if you want more AI-obsessed analysis, check out the podcast.  As I hope you can tell, I do the work!
	  
	  https://t.co/IrjorpPpSa ([View Tweet](https://twitter.com/labenz/status/1630292154768666628))