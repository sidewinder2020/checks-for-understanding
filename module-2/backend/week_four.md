## Week Four Recap

### Instructions
Fork this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

* What is a cookie?
small amnt of data stored on your local machine (usually consists of a user id), which tells the server that you have been to the site before

* What’s the difference between a session and a cookie?
sessions are encrypted cookies

* What’s a flash and when do you want to use flashes?
a small notice which allows you to notify the user, on the webpage, exactly what is/is not happening in the background - they are not permanent - you want a flash if someone creates something/updates something, etc.

* Why do people say “HTTP is stateless”?
because the sessions, and associated info, lies with the client, NOT the server

* What’s authentication? Explain.
authentication is allowing access to some/all pages of a website

* What’s the difference between authentication and authorization?
authentication is allowing access to the site, in general, authorization is dictating WHAT you are allowed to access/mess with

* What’s a before filter?
a line of code, at the top of your controller, to perform a method before any of the controller methods are performed UNLESS you specify with an except

* How do we keep track of a user once they’ve logged in?
user id/other info stored in a session

* When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
namespace - isn't necessary to have a controller, doesn't have an id (for say, admin) - admin is a great example
resource - has an id associated with both, controller is necessary - User is a nice one - mutliple users and varying content require an id

* At a high level, what tools can you use to implement authorization? How would you use them?
admin - mass implementation/destruction of certain features on the website
enums - assigning a default and an admin

* What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
an enum can be used to declare an overall state, and a contingency (or multiple) - for example: roles - default and admin

* What are some strategies you can use to keep your views DRY?
application layout - general template
partials - for ex: the edit/new pages are often VERY similar - minus
