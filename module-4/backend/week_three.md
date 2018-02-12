## Week Three - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR.

1. At a high level, what is Node?
allows you to work on js - run in the browser - except in your text editor
2. What is Express? What is Express similar to in the Ruby world?
express is a super lightweight framework - similar to rails (I mean - but rails does everything for you)
3. How do we setup a route when creating an API with Node and Express? Please provide a code snippet.
app.js
var meals = require('./routes/meals');
app.use('/api/v1/meals', meals);

create routes/meals.js
require files - then declare a route like:
router.get('/', function(req, res, next) {

  database.raw(
    'SQL QUERY'
  ).then(function(meals) {
    if(!meals.rows) {
      return res.sendStatus(404)
    } else {
      res.json(meals.rows)
    }
  })
})

4. What do we use Knex for?
grab information from the database
5. How **could** you organize your code to follow the MVC design pattern in your Quantified Self project?
You could set up your file structure, and refactor.  I refactored into a functional design, but you could have your models (the basic constructor functions), views(your ejs files - with basic html), and then your controllers with the methods performed on the router
6. How do you execute raw SQL in node?
database.raw('sql query here')
7. What are some advantages to having your front end and back end code live in separate applications? What are some disadvantages?
separate responsibility. If something breaks - it's easier to figure out where - especially without the prolific testing that existed in ruby.  However, CORS can be a pain in the ass, considering that it shouldn't be presenting too much of an issue with js to js, but it does anyway.  

#### Review  

8. Describe DNS.
9. What does writing clean code mean to you?
dry (but not too dry), maintainable, not too clever
10. If you were building an application that models hotels, what classes would you need? What classes would be responsible for what functionality? Hint: think about what tables you would need in the database, how those records would relate to each other, and good OOP.
6 classes, each with their own table:
hotel class
room class
amenities class
reservations class
guest class
employee class

1 hotel has many rooms, which has many amenities and has many reservations (the reservations table is also linked to the hotel class - which has many reservations)
reservations has 1 guest (The number of people in the room is stored on the reservations table, but the primary guest - name, cc (if they want the liability), contact info, is stored on the guest table - cleans
things up even if 1 rez has 1 primary guest)
and a reservation also has 1 employee, who belongs to a hotel (I don't think they move around?), but an employee can make many rez's
with the amenities - now that I'm thinking it through - I'd change it to be a json b column on the room table - easy to extract from - and booleans can get out of control quickly, considering the amount of amenities any 1 hotel room could offer
