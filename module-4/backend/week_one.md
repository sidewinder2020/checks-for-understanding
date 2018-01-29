## Week One - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR.

1. What's the most useful thing you learned from completing the intermission week work?
basic JS syntax/vocabulary - it helps me talk through problems, and set up simple code (that can be then be addressed/lends to my google-fu)

2. What are some tools to help debug JavaScript code?
dev tools: source code/debugger/console/element/network

3. What are some tools you need in order to unit test your JavaScript?
mocha - framework/chai - library

4. What is the syntax for invoking a function?
functionName() - the parentheses at the end

5. What is CORS?
Cross Origin Resource Sharing
it's a mechanism that allows you to HTTP resources from a separate domain than the domain from which your app was loaded

6. How do we enable CORS?
add an HTTP headers tag? I still need to enable - haven't pushed to production

7. What's `this` in JavaScript?
the entirety of whatever context you're working in - and all of the prototypes accessible to you for that context

8. What is Webpack and why is it useful?
a module bundler - it bundles all of the 'make it pretty' files in order to export them to your browser (it's a wannabe asset pipeline)

9. When/why do you want to use event delegation?
when we set up an event listener to a listen/react to a particular event

10. What's `npm` and what do we use it for?
a package manager for JS that we can use to manage all of the crap/local dependencies for a particular project

#### Review  
11. What's the MVC design pattern? Describe each part of MVC.
Model View Controller
M - relationships, queries on a class - talks to database
V - presentation of said data
C - grabs info from the model, and tailors it for the view

12. What are a few ways to optimize a Rails application?
tailoring how you store things in your database (including storing strings vs integers/indexing/etc.), and caching

13. What's a background worker? When would we want to use a background worker?
handles any delegated operations in the background (that we don't want taking up resources) - sidekiq was the one we used in mod 3

4. What is the syntax for invoking a function? Give an example.
function functionName( param(s) ) {
  what the function does
}

var function  = param => {
  stuff
}

5. What's `this` in JavaScript?
refers to the most applicable scope - allows you to call functions/whatever you want on the current scope

6. What is Webpack and why is it useful?
webpack is our new asset pipeline
it minimizes and concatenates our css, js, sass, svgs, etc - and packages them to be sent to the browswer

7. When/why do you want to use event delegation?
a good use case would be applying event delegation when assigning an event listener to the parent element (allowing you to listen for click/whatever events on any of the child elements - and even go as far as to tell you which one), instead of to 1 specific node

8. What's `npm` and what do we use it for?
node package manager - it's our new bundler
manage our packages/dependencies


#### Review  
9. What's the MVC design pattern? Describe each part of MVC.
model - view - Controller
model: handles the blueprint for the object, interacts with database
view: makes things pretty, holds template for the webpage
controller: gets info from the model - passes it to the view

10. What are a few ways to optimize a Rails application?
background workers, caching, indexing/compound indexing on the db, materialized views (and caching those), using activerecord over ruby (but SQL always wins - biased opinion)

11. What's a background worker? When would we want to use a background worker?
it handles tasks in the background - for example - you could have a background worker making your api calls, storing the info in your db for easy retrieval
-you could also use one when sending confirmation emails
