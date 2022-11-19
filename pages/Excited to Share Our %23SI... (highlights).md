title:: Excited to Share Our #SI... (highlights)
author:: [[@hypotext on Twitter]]
full-title:: "Excited to Share Our \#SI..."
category:: #tweets
url:: https://twitter.com/hypotext/status/1268218080993386497

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- Excited to share our #SIGGRAPH2020 paper!
	  
	  We’ve been building a new tool called Penrose, which takes a big step toward automatically visualizing mathematics.
	  
	  https://t.co/Tmkh92tHM0
	  
	  You just type math notation & Penrose magically comes up with a visualization for you. https://t.co/9QqXcCFend ([View Tweet](https://twitter.com/hypotext/status/1268218080993386497))
		- **Note**: Thread
	- There are a ton of great tools for making diagrams, but we found ourselves always either spending a long time drawing them in a graphical interface, or meticulously tweaking coordinates in code. (This timelapse from Adobe Illustrator is sped up 100x.) https://t.co/DxKNjPumrd ([View Tweet](https://twitter.com/hypotext/status/1268218084453744699))
	- The cool thing about Penrose is that you just describe the *relationships* you care about, and the tool automatically takes care of laying everything out. ([View Tweet](https://twitter.com/hypotext/status/1268218086173421569))
	- As a simple example, let's make a Venn diagram. In Penrose, we can just write some code like this:
	  
	  Set A, B
	  Intersecting(A, B)
	  Set C := Intersection(A, B)
	  Label A $\text{Circles}$
	  Label B $\text{Diagrams}$
	  Label C $\text{Venn Diagrams}$
	  
	  Hit go, and we get this picture. 
	  
	  ![](https://pbs.twimg.com/media/EZmPdc1WoAExBLh.jpg) ([View Tweet](https://twitter.com/hypotext/status/1268218087989444609))
	- If we don’t like it, we can just ask for another few. 
	  
	  ![](https://pbs.twimg.com/media/EZmPjOpXsAILbvA.jpg) 
	  
	  ![](https://pbs.twimg.com/media/EZmIGTKXYAAdxoJ.jpg) 
	  
	  ![](https://pbs.twimg.com/media/EZmIHR8X0AEN7mv.jpg) ([View Tweet](https://twitter.com/hypotext/status/1268218090191556608))
	- What we’ve written here is sort of like the “HTML” for our diagram, which specifies the content.  If we want to tweak the way it looks—or even its visual representation—we can also edit some CSS-like code. 
	  
	  ![](https://pbs.twimg.com/media/EZmPzp_WoAQGyos.jpg) ([View Tweet](https://twitter.com/hypotext/status/1268218092469006342))
	- By using different Styles, we can either just change the colors and line widths, or swap out the visualization to use arrows instead of circles. 
	  
	  ![](https://pbs.twimg.com/media/EZmQDBFXYAAX88S.jpg) ([View Tweet](https://twitter.com/hypotext/status/1268218094973071361))
	- Our paper shows how we can use the same approach to illustrate many different kinds of abstract ideas, including sets, functions, vectors, geometry, meshes, and ray tracing!
	  
	  For example, here we used Penrose to illustrate the same set of geometric statements in 3 ways. 
	  
	  ![](https://pbs.twimg.com/media/EZmQKa8WsAAqSZw.jpg) ([View Tweet](https://twitter.com/hypotext/status/1268218097296646154))
	- The way this all works under the hood is that we have 2 main pieces:
	  
	  💬 a LANGUAGE for defining a visual representation (think “CSS for math”) and
	  ⚙️ a SOLVER for exploring the space of diagrams (via optimization)
	  
	  More details in our #SIGGRAPH2020 paper: https://t.co/Tmkh92tHM0 
	  
	  ![](https://pbs.twimg.com/media/EZmZeO4WoAYWYBE.jpg) ([View Tweet](https://twitter.com/hypotext/status/1268218100136259586))
	- I personally think the Style language is really cool. It gives you a way to encode the visual subjectivity that you bring to the whiteboard, like telling the whiteboard what you mean as you draw. ([View Tweet](https://twitter.com/hypotext/status/1268218101667188741))
	- We hope to build Penrose into a platform for automatic illustration. For example:
	  
	  Could we automatically illustrate math textbooks & webpages?
	  Make interactive diagrams?
	  Create personal tutors?
	  
	  We’re a long way from reaching these goals, but think Penrose is a great first step! ([View Tweet](https://twitter.com/hypotext/status/1268218103932039170))
	- Thanks to my wonderful collaborators on the Penrose team: @wodenimoni, @maxkriegers, @dorma10, @wise_jenna, @JAldrichCMU, @joshsunshine, and @keenanisalive. ([View Tweet](https://twitter.com/hypotext/status/1268218105823723520))
	- Our system is not yet ready to use, but you can sign up for the mailing list to hear more: https://t.co/L4NEexeipc
	  
	  We’re looking to collaborate with educators and authors on making diagrams. If that sounds like you, get in touch here: https://t.co/MJwBm31WwQ ([View Tweet](https://twitter.com/hypotext/status/1268218107476291585))
	- And here's our SIGGRAPH talk: https://t.co/c0jYuDuWfJ ([View Tweet](https://twitter.com/hypotext/status/1298622601330405377))