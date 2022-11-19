title:: ✨ Here's How to Generate... (highlights)
author:: [[@levelsio on Twitter]]
full-title:: "✨ Here's How to Generate..."
category:: #tweets
url:: https://twitter.com/levelsio/status/1565731907664478209

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- ✨ Here's how to generate A.I. images with Stable Diffusion on your MacBook M1/M2 in less than 30 seconds for free:
		- **Note**: Thread
	- ⌨️ Type the commands below in terminal and press Enter:
	  
	  brew update
	  
	  brew install python
	  
	  git clone -b apple-silicon-mps-support https://t.co/d2NEJrQzHK (remove the linebreak before the URL here)
	  
	  👇 2/n
	  
	  (source: @bfirsh's https://t.co/roSnCRH9Kk) ([View Tweet](https://twitter.com/levelsio/status/1565732937139724288))
	- ⌨️ Type the commands below in terminal and press Enter:
	  
	  cd stable-diffusion
	  
	  mkdir -p models/ldm/stable-diffusion-v1/
	  
	  python3 -m pip install virtualenv
	  
	  python3 -m virtualenv venv
	  
	  source venv/bin/activate
	  
	  brew install Cmake protobuf rust
	  
	  👇 3/n ([View Tweet](https://twitter.com/levelsio/status/1565733231244087296))
	- ⌨️ Type the commands below in terminal and press Enter:
	  
	  pip install -r requirements.txt
	  
	  👇 4/n ([View Tweet](https://twitter.com/levelsio/status/1565733596949774336))
	- ⬇️ Now go to https://t.co/QUyItMNJMv, read and understand the license, then click "Access repository"
	  
	  Download sd-v1-4.ckpt (~4 GB) and save it under stable-diffusion/models/ldm/stable-diffusion-v1/model.ckpt
	  
	  👇 5/n ([View Tweet](https://twitter.com/levelsio/status/1565733945697787904))
	- 🎉 Done! Type this:
	  
	  python scripts/txt2img.py --n_samples 1 --n_iter 1 --plms --prompt "new born baby kitten. Hyper Detail, 8K, HD, Octane Rendering, Unreal Engine, V-Ray, full hd"
	  
	  If it works, the image is saved under /outputs/txt2img-samples 
	  
	  Reply w/ your pics here!
	  
	  👇 6/n 
	  
	  ![](https://pbs.twimg.com/media/FbqbBM8XkAAwyIW.png) ([View Tweet](https://twitter.com/levelsio/status/1565734786660024320))
	- 😭 If it doesn't work, reply with a screenshot here and I and other people will try help you to set it up!
	  
	  Make sure you upgraded MacOS to the latest version (double check). And make sure you actually have an M1/M2 MacBook (those are the latest MacBooks)
	  
	  👇 7/n ([View Tweet](https://twitter.com/levelsio/status/1565735024720232449))
	- Image credits from original tweet from blog post by @Alber_RomGar 
	  
	  Face: HollyB#1382 (portrait)
	  Ship: HollyB#1382 (seascape)
	  City: Joe#5956 (cityscape)
	  
	  https://t.co/hhoZlAzf3G ([View Tweet](https://twitter.com/levelsio/status/1565735549217931264))
	- Again credits to @bfirsh for figuring all this out, I just rewrote his tutorial for Twitter putting the "brew install Cmake protobuf rust" first cause I needed that to make it work
	  
	  https://t.co/roSnCRH9Kk ([View Tweet](https://twitter.com/levelsio/status/1565736248366465025))
	- If you want to adjust the detail (and speed of generating it) here's some tips to use --ddim_steps param
	  
	  https://t.co/1anyryiCka ([View Tweet](https://twitter.com/levelsio/status/1565736376896724994))
	- And here's some random text prompts I collected that I add at the end of every prompt I type that make it very pretty:
	  
	  cinematic photo, highly detailed, cinematic lighting, ultra-detailed, ultrarealistic, photorealism, 8k, octane render ([View Tweet](https://twitter.com/levelsio/status/1565736603062079489))
	- cyberpunk lights, Hyper Detail, 8K, HD, Octane Rendering, Unreal Engine, V-Ray, full hd ([View Tweet](https://twitter.com/levelsio/status/1565736628693471232))
	- cyberpunk, abstract, full hd render + 3d octane render +4k UHD + immense detail + dramatic lighting + well lit + black, purple, blue, pink, cerulean, teal, metallic colours, + fine details + octane render + 8k ([View Tweet](https://twitter.com/levelsio/status/1565736655323021314))
	- ultra photoreal , photographic, concept art, cinematic lighting, cinematic composition, rule of thirds , mysterious, eerie, cinematic lighting, ultra-detailed, ultrarealistic, photorealism, 8k, octane render, ([View Tweet](https://twitter.com/levelsio/status/1565736684284788740))
	- breathtaking detailed concept art painting art deco pattern - blue flowers with anxious piercing eyes and blend of flowers and birds, by hsiao - ron cheng and john james audubon, bizarre compositions, exquisite detail, extremely moody lighting, 8 k ([View Tweet](https://twitter.com/levelsio/status/1565736710893445121))
	- painted by greg rutkowski makoto shinkai takashi takeuchi studio ghibli, akihiko yoshida ([View Tweet](https://twitter.com/levelsio/status/1565736742090641409))
	- If you quit the Terminal or reboot, you get kicked out of the virtualenv, to get back in type:
	  
	  source venv/bin/activate 
	  
	  And run you rprompt
	  
	  python scripts/txt2img.py --n_samples 1 --n_iter 1 --plms --prompt "your text here" ([View Tweet](https://twitter.com/levelsio/status/1565736856393863170))
	- Oh and there's an NSFW filter, but you can disable it easily by editing some files:
	  
	  https://t.co/wXRaW6use4 
	  
	  ![](https://pbs.twimg.com/media/FbqdlkgWIAEr30r.jpg) ([View Tweet](https://twitter.com/levelsio/status/1565737122736259074))