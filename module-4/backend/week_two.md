## Week Two - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR.

1. What's one difference between ES5 and ES6?
syntax for interpolation
ES5 - combo of +'s, empty strings for spaces, and calling variables with their properties
ES6 - backticks and ${}

2. What's the difference between asynchronous and synchronous JavaScript?
JS is synchronous - it's not a multi-threaded language
it only appears to be multi-threaded because the browser's api allows for consumption of functions with callbacks - which get passed along back into the status queue, making it appear as if it can perform multiple tasks at one time
AKA: it's a fraud

3. What are the four pillars of Object Oriented programming?
shahada, sawm, hajj, and... wait, those are the 5 pillars of islam.

Encapsulation - wrapping methods and functions in a class
Abstraction - creating classes, objects, etc. in order to separate them by functionality and interfaces
Inheritance - can reuse code of existing objects, which cuts back on redundancy
Polymorphism - you can use the same interface for different data types (active record assoc. and arrays, for example)

4. What are some tools available in JavaScript to help you write object oriented code?
You can create 'objects' in JS - with properties, and properties can even be functions on that particular object.  You can create constructor functions, which are basically an object factory. It has the ability create instances that have both state and behavior.

5. What are some key concepts to be aware of when refactoring your JavaScript?
functional refactoring *seems* to be preferred? Ajax requests, event listeners, the basic model, and response handlers are separated by their function

6. What's a callback function and what are some reasons when we use/need callback functions?
a callback function is a function called by another function - we might use one inside of an API call, so that the browser's API takes care of the fetch call, and then the callback function is passed along to re-enter the status queue when the queue is empty

7. What's the scope of variables in Javascript?
the scope of a variable refers to the context in which the variable is accessible.  Whether that is global, only within a particular function, due to where the variable is declared, etc

8. What's the difference between `==` and `===` in JavaScript?
loose equality (==) vs strict equality (===)
loose equality compares one piece to another, but *can* convert the type of the values to match - which I think we can all agree, is cheating
strict equality (aka: the best equality) - does not convert either value to 'force' a match

9. Why do front end frameworks exist?
because JS is s%i*, and was written in like, 10 days.  You need an interpreter/someone who can compress/sometimes completely overhaul the existing libraries, because even those are dubious, and frameworks are used to provide some semblance of convention and structure in an otherwise malleable language

#### Review  

10. Why do people say "HTTP is stateless"?
the connection between the server and the browser ends once the transaction does - it's not held in memory - you have to tell it the state every time it comes back

11. Describe a RESTful API.
an api where the endpoints follow restful patterns - verb/uri patterns

12. What are some main characteristics of a team following an agile workflow?
They take one piece at a time, then break down the process, until that piece is finished.  Then take another piece, go through the process, and so on.
They tend to have a more fluid, and collaborative, style because they have to communicate more often, as opposed to breaking the project into chunks at the beginning, and working those chunks, independently, from start to finish.

13. What are some advantages **and** disadvantages to using OAuth to authenticate a user?
advantages: You aren't storing a password, you aren't responsible for a lot of personal info, it takes care of the authentication
disadvantages: it's a pain in the $#% to set up, having to fight with token timeouts, if you don't have a user profile IN ADDITION to oauth - you don't have alot of info about your user, you limit who can use your site based upon which oauth you're using - and if they have accts with the choices offered
