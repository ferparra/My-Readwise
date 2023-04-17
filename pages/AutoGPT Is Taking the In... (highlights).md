title:: AutoGPT Is Taking the In... (highlights)
author:: [[@SullyOmarr on Twitter]]
full-title:: "AutoGPT Is Taking the In..."
category:: #tweets
url:: https://twitter.com/SullyOmarr/status/1645482778677452805

- Highlights first synced by [[Readwise]] [[Apr 13th, 2023]]
	- AutoGPT is taking the internet by storm. Its everywhere.
	  
	  They’re basically AI agents that run by itself, and complete tasks for you.
	  
	  The best part is you can set it up yourself, and have your own 🤖 doing your bidding for you in less 30 minutes.    
	     
	  Heres how: 
	  
	  ![](https://pbs.twimg.com/media/FtXt3ZwXoAsLVNO.jpg) ([View Tweet](https://twitter.com/SullyOmarr/status/1645482778677452805))
		- **Note**: Thread
	- Ok first up: You will need to know how to run terminal commands. Thats about it. 
	  
	  Then go and do these things :
	- Then you want start by cloning the repo https://t.co/L6M3RrbfLA
	  
	  `git clone https://t.co/L6M3RrbfLA`
	  
	  then navigate into it with `cd Auto-GPT` 
	  
	  ![](https://pbs.twimg.com/media/FtXt4PMXoAgkrUb.jpg) ([View Tweet](https://twitter.com/SullyOmarr/status/1645482793609097217))
	- You will see a file called .env.template, put your openai api key here.
	  
	  Then duplicate the file, and rename it to just .env 
	  
	  ![](https://pbs.twimg.com/media/FtXt4wjXoAgq-Qw.jpg) ([View Tweet](https://twitter.com/SullyOmarr/status/1645482803365068800))
	- Once done, you can run the command `pip install -r requirements.txt` 
	  
	  This will download all the python packages. Remember you need python downloaded.
	  
	  Ok now we’re almost done and ready to get your AI going, but before make sure you: ([View Tweet](https://twitter.com/SullyOmarr/status/1645482810432528399))
	- Have docker running! I use docker desktop, and it works perfectly on windows and mac. It just needs to be on. 
	  
	  Don't worry you don't need to download any containers or anything. 
	  
	  ![](https://pbs.twimg.com/media/FtXt54_XoAASLBL.jpg) ([View Tweet](https://twitter.com/SullyOmarr/status/1645482822252077059))
	- Then you run python scripts/main.py and the terminal will start to prompt you. 
	  
	  You can do continuous mode if you want it go fully autonomous, or you can sit there and approve each action yourself. 
	  
	  For continuous mode:
	  `python scripts/main.py --continuous` 
	  
	  ![](https://pbs.twimg.com/media/FtXt6m5XoAcXgKB.jpg) ([View Tweet](https://twitter.com/SullyOmarr/status/1645482833824079874))
	- And thats it to get it up and running!
	  
	   But it’s not perfect and you’ll run into issues a decent amount of times, so here’s what I did to make the process smooth. ([View Tweet](https://twitter.com/SullyOmarr/status/1645482836097474572))
	- Goals:
	  Since AutoGPT is so new, its not perfect (understandably) so setting the right goals will be the difference between accomplishing tasks and failing them. ([View Tweet](https://twitter.com/SullyOmarr/status/1645482844595134490))
	- In my researchGPT i actually gave it a very basic set of goals.
	  
	  The second one seems a lot more in-depth right?
	  
	  Well its actually worse because for now its too in-depth. AutoGPT will begin to start looping and getting stuck at the planning phase. You wont get any output at all 
	  
	  ![](https://pbs.twimg.com/media/FtXt7qEWYAA4Prb.jpg) 
	  
	  ![](https://pbs.twimg.com/media/FtXt7pfWAAE5Y96.jpg) ([View Tweet](https://twitter.com/SullyOmarr/status/1645482851855474694))
	- So as a rule of thumb:
	  1) start simple, test the output, and then adjust your goals. 
	  This isn’t a science per say, there is usually a lot of back and forth. 
	  
	  This isn't perfect at all but amazing nonetheless. ([View Tweet](https://twitter.com/SullyOmarr/status/1645482858948050946))
	- Saving to files:
	  
	  Since autoGPT can write to files, we need to nudge it in the right direction. 
	  
	  In my example, I just ask it to save the analysis, and this is usually good enough. ([View Tweet](https://twitter.com/SullyOmarr/status/1645482860764176404))
	- Sometimes you want it to save for each goal, so you can ask it that. 
	  
	  Something like:
	  Goal 1 : find the top 10 shoe brands,  Save the output.
	  Goal 2: and do SWOT analysis. of each brand, save it ([View Tweet](https://twitter.com/SullyOmarr/status/1645482862903271433))
	- General issues:
	  Sometimes you’ll see AutoGPT loop, and I try to monitor it closely. 
	  
	  If it starts to loop for more than 2-3 minutes, it usually means its stuck and you’ll have to restart the process again. ([View Tweet](https://twitter.com/SullyOmarr/status/1645482864794902528))
	- To get the full potential of AutoGPT You WILL NEED GPT4 API access. 
	  
	  If you are just using gpt3.5 the depth of agents/responses might let you down. 
	  
	  I know most of you don’t have access which really sucks, so make sure you join the waitlist. ([View Tweet](https://twitter.com/SullyOmarr/status/1645482866757754882))
	- Feel free to leave comments and ask questions here.  I'll try to answer questions the best I can. ([View Tweet](https://twitter.com/SullyOmarr/status/1645482868913602563))