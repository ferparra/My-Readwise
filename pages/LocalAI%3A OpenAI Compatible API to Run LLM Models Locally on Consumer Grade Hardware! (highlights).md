title:: LocalAI: OpenAI Compatible API to Run LLM Models Locally on Consumer Grade Hardware! (highlights)
author:: [[Create Post]]
full-title:: "LocalAI: OpenAI Compatible API to Run LLM Models Locally on Consumer Grade Hardware!"
category:: #articles
url:: https://www.reddit.com/r/selfhosted/comments/12w4p2f/localai_openai_compatible_api_to_run_llm_models/

- Highlights first synced by [[Readwise]] [[May 7th, 2023]]
	- 🚀 LocalAI is taking off! 🚀
	  
	  We just hit 330 stars on GitHub and we’re not stopping there! 🌟
	  
	  LocalAI is the OpenAI compatible API that lets you run AI models locally on your own CPU! 💻 Data never leaves your machine! No need for expensive cloud services or GPUs, LocalAI uses llama.cpp and ggml to power your AI projects! 🦙
	  
	  LocalAI supports multiple models backends (such as Alpaca, Cerebras, GPT4ALL-J and StableLM) and works seamlessly with OpenAI API. 🧠 Join the LocalAI community today and unleash your creativity! 🙌
	  
	  GitHub: [https://github.com/go-skynet/LocalAI](https://github.com/go-skynet/LocalAI)
	  
	  We are also on discord! Feel free to join our growing community!
	  
	  Update 27-04:
	  
	  Twitter: [https://twitter.com/LocalAI_API](https://twitter.com/LocalAI_API) HN Link: [https://news.ycombinator.com/item?id=35726934](https://news.ycombinator.com/item?id=35726934)
	  
	  •   Added e2e example to set up LocalAI + chatbot-ui [https://github.com/go-skynet/LocalAI/tree/master/examples/chatbot-ui](https://github.com/go-skynet/LocalAI/tree/master/examples/chatbot-ui)
	    
	  •   K8sGPT is now supporting LocalAI, for Kubernetes cluster analysis: [https://medium.com/@tyler_97636/k8sgpt-localai-unlock-kubernetes-superpowers-for-free-584790de9b65](https://medium.com/@tyler_97636/k8sgpt-localai-unlock-kubernetes-superpowers-for-free-584790de9b65)
	    
	  •   Kairos ([https://github.com/kairos-io/kairos](https://github.com/kairos-io/kairos)) plans to easily integrate LocalAI for On prem Kubernetes cluster monitoring and analysis.
	    
	  
	  Update 25-04:
	  
	  E2E example with GPT4ALL-j: [https://github.com/go-skynet/LocalAI#example-use-gpt4all-j-model](https://github.com/go-skynet/LocalAI#example-use-gpt4all-j-model)
	  
	  Update 24-04:
	  
	  Thank you for your feedback! We just crossed 700 stars! I'm currently reading the comments and updating our docs to address all the questions you raised. Stay tuned, and let's democratize AI together and spread the word! I've submitted it to HN [https://news.ycombinator.com/item?id=35726934](https://news.ycombinator.com/item?id=35726934) !
	  
	  I want to talk about LocalAI's goals, as it is a community project with no company behind it. On a personal note, I believe that AI should be accessible to anyone, and ggerganov's ggml is a great piece of work that serves as the foundation for LocalAI, so a lot of credit goes to him as well. With LocalAI, my main goal was to provide an opportunity to run OpenAI-similar models locally, on commodity hardware, with as little friction as possible. There is a significant fragmentation in the space, with many models forked from ggerganov's implementation, and applications built on top of OpenAI, the OSS alternatives make it challenging to run different models efficiently on local hardware. The API model allows to abstract from these complexities, so that anyone can focus on plugging AI to the software, and LocalAI takes care of the interface. One of the main reasons for the existence of LocalAI is also to provide a strong solution, hardware "friendly" (so I can just run it locally!) in the open-source ecosystem that avoids vendor lock-in, as I believe that open-source software should have (hopefully better) alternatives to proprietary, closed solutions. I want to have ownership of my data first!
	  
	  Here are answers to some of the most common questions I've seen in the comments:
	  
	  •   How do I get models? Most ggml-based models should work, but newer models may require additions to the API. If a model doesn't work, please feel free to open up issues. However, be cautious about downloading models from the internet and directly onto your machine, as there may be security vulnerabilities in lama.cpp or ggml that could be maliciously exploited. Some models can be found on Hugging Face: [https://huggingface.co/models?search=ggml](https://huggingface.co/models?search=ggml), or models from gpt4all should also work: [https://github.com/nomic-ai/gpt4all](https://github.com/nomic-ai/gpt4all). An e2e example is here: [https://github.com/go-skynet/LocalAI#example-use-gpt4all-j-model](https://github.com/go-skynet/LocalAI#example-use-gpt4all-j-model)
	    
	  •   What's the difference with Serge, or XXX? LocalAI is a multi-model solution that doesn't focus on a specific model type (e.g., llama.cpp or alpaca.cpp), and it handles all of these internally for faster inference. It is also easy to set up locally.
	    
	  •   Can I use it with a Discord bot, or XXX? Yes! If the client uses OpenAI and supports setting a different base URL to send requests to, you can use the LocalAI endpoint. This allows to use this with every application that was supposed to work with OpenAI, but without changing the application!
	    
	  •   Can this leverage GPUs? Not currently, as ggml doesn't support GPUs yet: [https://github.com/ggerganov/llama.cpp/discussions/915](https://github.com/ggerganov/llama.cpp/discussions/915).
	    
	  •   Where is the webUI? We are working on to have a good out of the box experience - however as LocalAI is an API you can already plug it into existing projects that provides UI interfaces to OpenAI's APIs. There are several already on github, and should be compatible with LocalAI already (as it mimics the OpenAI API)
	    
	  •   Does it work with AutoGPT? AutoGPT currently doesn't allow to set a API, but there is a PR open for it, so this should be possible soon!
	    
	  
	  Short-term roadmap update:
	  
	  •   Integrate with an already existing web UI.
	    
	  •   Allow configuration of defaults for models.
	    
	  •   Enable automatic downloading of models from a curated gallery, with only free-licensed models.
	    
	  •   Release binary versions.
	    
	  
	  For updates, join Discord ([https://discord.gg/uJAeKSAGDy](https://discord.gg/uJAeKSAGDy)), you can also follow me @ Twitter ( [https://twitter.com/mudler_it/](https://twitter.com/mudler_it/) ) and @ Github ( [https://github.com/mudler/](https://github.com/mudler/) ) ([View Highlight](https://read.readwise.io/read/01gzspfn5w5808j185n7y0m3gm))