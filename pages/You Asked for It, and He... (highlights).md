title:: You Asked for It, and He... (highlights)
author:: [[@charlierward on Twitter]]
full-title:: "You Asked for It, and He..."
category:: #tweets
url:: https://twitter.com/charlierward/status/1638303596595892224

- Highlights first synced by [[Readwise]] [[Mar 24th, 2023]]
	- You asked for it, and here it is. 
	  
	  "How I built a functioning Chrome Extension in 10 steps and 45 minutes, with no coding experience. Using ChatGPT + Replit." 
	  
	  Let's dive in people. 👾 https://t.co/DxGXx4yCJ0 ([View Tweet](https://twitter.com/charlierward/status/1638303596595892224))
		- **Note**: Thread
	- (Before we start: to re-iterate, I *cannot code*. I've never shipped a product outside of basic no-code. While I have experience in the tech industry, it is as a PM/UX Researcher. 
	  
	  I know the name of certain things, e.g. an IDE, but I am not a developer, not even a hobbyist. ([View Tweet](https://twitter.com/charlierward/status/1638303598005067780))
	- Step 1: Choose your idea
	  
	  For a while, I'd wanted to make a Chrome Extension for members of a founder community I run (https://t.co/sCxGt0K0N5) where it displayed startup related quotes with each new browser tab. ([View Tweet](https://twitter.com/charlierward/status/1638303599263358978))
	- Using my buddy @sab8a's "make something people search for" framework, I fired up @ahrefs to find high volume keywords related to what I wanted. 
	  
	  Eventually, I found "marketing quotes" (18k global searches per month), a topic I know is important to many of our members/audience. 
	  
	  ![](https://pbs.twimg.com/media/FrwR2-sXgAIS9pC.jpg) ([View Tweet](https://twitter.com/charlierward/status/1638303600660164610))
	- After checking the Chrome Web Store (where I eventually submitted the extension), I couldn't find anything with that name or closely related to its functionality, so that was good enough for me. 
	  
	  In the words of a famous egghead: "it's time to build". https://t.co/NWNvrgvIka ([View Tweet](https://twitter.com/charlierward/status/1638303602740547584))
	- Step 2 - Setup a @Replit account
	  
	  Replit is a cloud based IDE (Integrated Development Environment) where you can write, run and deploy code. 
	  
	  The beauty is you don't have to spend time setting up your dev environment or installing code: making it great for beginners. I use Pro. 
	  
	  ![](https://pbs.twimg.com/media/Frwme4DWwAIq-ZC.jpg) ([View Tweet](https://twitter.com/charlierward/status/1638303604225236995))
	- Step 3 - Get ChatGPT Plus
	  
	  Go to https://t.co/V3BrBcGsy5 and upgrade to Plus for $20/month - so you can use their most powerful new model, GPT-4. 
	  
	  It is noticeably more nuanced, intelligent and useful than its predecessor, GPT-3 IMHO. ([View Tweet](https://twitter.com/charlierward/status/1638303606184058883))
	- Step 4 - Do your first prompt
	  
	  Select 'GPT-4' from the dropdown menu at the top. I then wrote what I wanted to build, its functionality, my setup and that I wanted a step by step, beginners guide, including code needed. 
	  
	  This doesn't have to be perfect - just refine it later. 
	  
	  ![](https://pbs.twimg.com/media/FrxosSyWYAYwF27.jpg) ([View Tweet](https://twitter.com/charlierward/status/1638303607706484740))
	- Step 5 - Create a new Repl in Replit
	  
	  Think of a Repl as a folder for your project, where your code files will live. When you setup a new one, it'll ask you what 'Template' (aka language) you want - for a Chrome Extension it's usually 'HTML, CSS, JS'. 
	  
	  ![](https://pbs.twimg.com/media/Frwkc7MWIGQIBBr.jpg) ([View Tweet](https://twitter.com/charlierward/status/1638303609233235973))
	- From your original prompt, ChatGPT should have already told you which 'Template' to select. If it doesn't, just follow up with this question. 
	  
	  Remember to name your Repl, describe it if you want, and I'd usually advise setting it to 'Private'. ([View Tweet](https://twitter.com/charlierward/status/1638303610730696708))
	- Important note: ChatGPT is (currently) only trained up until 2021, so some of its knowledge is slightly out of date, including on Replit's interface. 
	  
	  Just tell it when it's obviously wrong (e.g. where a button is) and it'll usually apologise and give you better advice. ([View Tweet](https://twitter.com/charlierward/status/1638303612102139907))
	- Some more quick tips:
	- Step 6 - Create files & paste in your code
	  
	  ChatGPT should already have told you the exact files to create in your Repl, and the code to paste into them. If it isn't this specific, just ask it to do this.
	  
	  Here's an example of my setup on Replit. Click 'Run' when you're done. 
	  
	  ![](https://pbs.twimg.com/media/Frwn_qmXoAAlgt3.jpg) ([View Tweet](https://twitter.com/charlierward/status/1638303615315070978))
	- Step 7 - Debugging
	  
	  This is another area ChatGPT is very impressive. After you clicked 'Run', the 'Webview' on the right should display something resembling what you're trying to build. However, often, there is something wrong. ([View Tweet](https://twitter.com/charlierward/status/1638303616745308160))
	- If you get a specific error message, paste that into ChatGPT, and it'll often give you the right answer, or options. 
	  
	  If it's not a specific issue, describe the problem, or just say you have a problem. Then try the different options you're provided. Ask it to simplify if needed. ([View Tweet](https://twitter.com/charlierward/status/1638303618305609728))
	- Step 8 - Export your files
	  
	  As we've built a Chrome Extension, you can't deploy directly from Replit (you can for other things). So you must export your files, zip them, then upload to Chrome DevTools. ([View Tweet](https://twitter.com/charlierward/status/1638303619664543745))
	- To do this, first click on the three dots in the left-hand side of your Repl, and click 'Download as zip'. 
	  
	  For certain projects, if you also need to add additional files (such as images) to this, unzip, add the files and then zip it again. I use Archive Utility for this on Mac. 
	  
	  ![](https://pbs.twimg.com/media/FrwsaElWIA0X6gE.jpg) ([View Tweet](https://twitter.com/charlierward/status/1638303621019234304))
	- Step 9 - Submit to the Chrome Web Store
	  
	  Next, using Google's Chrome browser (if you don't have it, download it), you need to create a Chrome Web Store developer account here: https://t.co/ncNSm2OckG. 
	  
	  This will cost a one-time $5 registration fee. After that, sign-up. 
	  
	  ![](https://pbs.twimg.com/media/FrxkD7jWYAAbwZD.jpg) ([View Tweet](https://twitter.com/charlierward/status/1638303622516580353))
	- After filling in your details in 'Account', click 'Items' on the left, then 'New Item'. After this, you can upload your .zip file. 
	  
	  If you struggle here, as always, just explain your issue and ChatGPT should tell you how to solve it. My issue was that I zipped the file wrong. 🤦‍♂️ 
	  
	  ![](https://pbs.twimg.com/media/FrxkqlJWcAEcFNJ.jpg) ([View Tweet](https://twitter.com/charlierward/status/1638303623972003840))
	- Fill in all the fields required, troubleshoot any issues, and submit!
	  
	  Congrats, you've created your first Chrome Extension MVP. It can take up to a few weeks for them to either accept you, or give you feedback on what to update. ([View Tweet](https://twitter.com/charlierward/status/1638303625679101953))
	- Step 10 - Share your project
	  
	  Lots of other makers want to see how you built your Chrome Extension, or anything else you made. Remember to share a breakdown to inspire and educate us.
	  
	  I feel like there's a lot of cool shit to come. 🔥 ([View Tweet](https://twitter.com/charlierward/status/1638303626975117314))
	- Lots of people are mocking people building MVPs on ChatGPT right now, but ignore the haters. 
	  
	  Whether people like it or not, the genie's out of the bottle. When a 10x productivity improvement comes along, which is very rare, you need to grab the opportunity with both hands. ([View Tweet](https://twitter.com/charlierward/status/1638303628308955137))
	- I want to once again shoutout @joeprkns for his original inspiration on this build and this thread. 
	  
	  Props to him. The 🐐. And thanks to @OpenAI (I think) for putting a dent in the universe.
	  
	  https://t.co/6t944w8LTF ([View Tweet](https://twitter.com/charlierward/status/1638303629709803521))
	- Finally, a thank you for reading. I don't have a Soundcloud, but if you want to join a community of 140+ amazing founders, come and join us at https://t.co/sCxGt0K0N5 🍜 (@RamenClubHQ) ([View Tweet](https://twitter.com/charlierward/status/1638303631597248514))
	- If you enjoyed this thread, follow my handle: @charlierward for more tweets like this. 
	  
	  And if you're feeling extra generous, like and RT the original post. ❤️‍🔥
	  
	  https://t.co/OihrzVQ3xv ([View Tweet](https://twitter.com/charlierward/status/1638306456272289792))
	- Something I found interesting, which may be new:
	  
	  The easiest part of the process was creating the code. 
	  
	  The hard parts were dealing with all the intermediary steps like making the right files in Replit, and entering/uploading the right information to the Chrome Web Store. ([View Tweet](https://twitter.com/charlierward/status/1638317952133996545))
	- Again, this is talking about a very simple MVP. I'm not arguing this has solved software development. 
	  
	  But I'd wager that the above tweet was not true even 1 year ago. ([View Tweet](https://twitter.com/charlierward/status/1638322471798468608))
	- The @usefathom dashboard for https://t.co/sCxGt0K0N5 😹 
	  
	  ![](https://pbs.twimg.com/media/Fr0SP_QXoAAzaaF.jpg) ([View Tweet](https://twitter.com/charlierward/status/1638486054435954690))
	- 1k bookmarks 🎉 https://t.co/eVxfS3UdOZ ([View Tweet](https://twitter.com/charlierward/status/1638486573061754882))