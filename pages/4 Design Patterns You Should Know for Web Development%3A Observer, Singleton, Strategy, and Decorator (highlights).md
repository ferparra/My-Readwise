title:: 4 Design Patterns You Should Know for Web Development: Observer, Singleton, Strategy, and Decorator (highlights)
author:: [[freecodecamp.org]]
full-title:: "4 Design Patterns You Should Know for Web Development: Observer, Singleton, Strategy, and Decorator"
category:: #articles
url:: https://www.freecodecamp.org/news/4-design-patterns-to-use-in-web-development/

- Highlights first synced by [[Readwise]] [[Nov 19th, 2022]]
	- The Singleton Design PatternThe singleton pattern only allows a class or object to have a single instance and it uses a global variable to store that instance. You can use lazy loading to make sure that there is only one instance of the class because it will only create the class when you need it.
	- The Strategy Design PatternThe strategy is pattern is like an advanced version of an if else statement.  It's basically where you make an interface for a method you have in your base class. This interface is then used to find the right implementation of that method that should be used in a derived class. The implementation, in this case, will be decided at runtime based on the client.
	- The Observer Design PatternIf you've ever used the MVC pattern, you've already used the observer design pattern. The Model part is like a subject and the View part is like an observer of that subject. Your subject holds all of the data and the state of that data. Then you have observers, like different components, that will get that data from the subject when the data has been updated.
	- The Decorator Design PatternUsing the decorator design pattern is fairly simple. You can have a base class with methods and properties that are present when you make a new object with the class. Now say you have some instances of the class that need methods or properties that didn't come from the base class.