title:: There's a New Programmin... (highlights)
author:: [[@jeremyphoward on Twitter]]
full-title:: "There's a New Programmin..."
category:: #tweets
url:: https://twitter.com/jeremyphoward/status/1653924474536984577

- Highlights first synced by [[Readwise]] [[May 4th, 2023]]
	- There's a new programming language in town - it's Mojo! I'm more than a little excited about it. It's Python, but with none of Python's problems.
	  
	  You can write code as fast as C, and deploy small standalone applications like C.
	  
	  My post is below, and a 🧵
	  https://t.co/0IWGqcpEY7 ([View Tweet](https://twitter.com/jeremyphoward/status/1653924474536984577))
		- **Note**: Thread
	- Python is the language that I have used for nearly all my work over the last few years. It is a beautiful language. It has an elegant core on which everything else is built.
	  
	  But it comes with a downside: performance. It's thousands of times slower than C. ([View Tweet](https://twitter.com/jeremyphoward/status/1653924477682745344))
	- Python programmers learn to avoid using Python for the implementation of performance-critical sections, instead using Python wrappers over C, FORTRAN, Rust, etc.
	  
	  But this “two-language” approach has serious downsides. It's complex, hard to debug or profile, & hard to deploy. ([View Tweet](https://twitter.com/jeremyphoward/status/1653924480580984834))
	- Also, it leaves a lot of performance on the table. That's why @PyTorch, @Tensorflow, and #jax don't use Python for anything fast - they use separate compilers for Python DSL's or subsets.
	  https://t.co/iGsS00HYvJ ([View Tweet](https://twitter.com/jeremyphoward/status/1653924484100026368))
	- Mojo is "syntax sugar for MLIR". It has a small foundation which basically provides a simple way to access MLIR from a Python-like language, and then everything else is written on top of that.
	  https://t.co/r3BvsSOERQ ([View Tweet](https://twitter.com/jeremyphoward/status/1653924487396458497))
	- A Mojo trick is to opt in to a faster “mode” by using “fn” instead of “def” - as a result Mojo can create optimised machine code to implement your function. & use “struct” instead of “class” to tightly pack your attrs in memory, to avoid pointer chasing ([View Tweet](https://twitter.com/jeremyphoward/status/1653924490911576065))
	- Mojo isn't finished - but what's there is already mind-blowing, and it has been created by a very small team in a very short time. This shows the benefits of using carefully architected foundations, based on @clattner_llvm's years of experience with Clang, LLVM, and Swift. ([View Tweet](https://twitter.com/jeremyphoward/status/1653924494267002880))
	- There are lots of other great alternatives to getting high performance and the benefits of elegant programming language, including @JuliaLanguage, #cython, and @numba_jit.
	  
	  These all have their place, but they're not perfect. Eg here's my thoughts on Julia
	  https://t.co/sSpHQ4oMGt ([View Tweet](https://twitter.com/jeremyphoward/status/1653924497312067585))
	- In particular, Mojo is the first to solve deployment.
	  
	  A Mojo app can be compiled into a small, standalone, fast-starting binary. This is a game changer! Think about the things you could do if you could create small fast tools quickly & easily, & distribute them in a single file. ([View Tweet](https://twitter.com/jeremyphoward/status/1653924500789166080))
	- Mojo is *far more* than a language for AI/ML applications. It’s actually a version of Python that allows us to write fast, small, easily-deployed applications that take advantage of all available cores and accelerators!
	  https://t.co/GANS2HBap8 ([View Tweet](https://twitter.com/jeremyphoward/status/1653924503876141056))
	- If you want to know more or have any questions, check out the full blog post, which has much more detail than this thread:
	  https://t.co/0IWGqcpEY7 ([View Tweet](https://twitter.com/jeremyphoward/status/1653924506996740097))