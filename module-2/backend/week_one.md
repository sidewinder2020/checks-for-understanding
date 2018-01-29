## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

1. List the five common HTTP verbs and what the purpose is of each verb.
Get - retrieve information
put - ask the server that the information, being passed, be stored under the supplied Request-URI (a particular location)
post - ask the server to accept the information being passed
delete - delete information
options - request for information about the communication options available on the request/response chain (like put, in a particular location/page?)
2. What is Sinatra?
domain specific language, used for writing web applications
4. What is MVC?
model, view, controller: used for creating a web application
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
allows other programmers to easily understand your routes, they are built into sinatra
6. What types of variables are accessible in our view templates without explicitly passing them?
instance variables
7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?

```ruby
get '/horses' do
  @count = 1
  horse = "Mr. Ed"
  erb :index
end
```

9. What's the purpose of ERB?
interpolation
10. Why do I need a development AND test database?
<<<<<<< HEAD
the tests rely on a mock database, but the development relies on the database, created from the migration - user doesn't need access to the test database
11. What's responsive design?
design and development respond to the user's interactions
12. What is CRUD and why is it important?
Create, Read, Update, Delete - the 4 components of the web - it makes up what the web is composed of
13. What does HTTP stand for?
hypertext transfer protocol
14. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
<% %> - used to perform ruby within the html, an enumerable, for example
<%= %> - used to pull in a method
15. What's an ORM?
Object relational mapping
16. What's the most commonly used ORM in ruby (Sinatra & Rails)?
activerecord
17. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.

get '/' do - dashboard
get '/restaurants' do - navigate to restaurant index
get '/restaurants/new' do - navigates to the new page (create a new restaurant)
post '/restaurants' do - creates a new instance, then navigates back to the index
get '/restaurants/:id' do - find a specific restaurant, according to id, and display that page
get '/restaurants/:id/edit' do - navigate to the edit page for a specific restaurant
put '/restaurants/:id' do |id| - update the restaurant's information, found by id, and navigating back to that restaurant's page
delete '/restaurants/:id' do |id| - destroy a particular restaurant, found by id, and navigating back to the index page

18. What's a migration?
a template to create the database from the CSV
19. When you create a migration, does it automatically modify your database?
no, you need to tell your program to create a new database, which will follow your migration
20. How does a model relate to a database?
the model allows you to pull information from the database
21. What's the difference between agile workflow and waterfall method?
Agile works piece by piece, following through with step 1, then step 2, etc. of the process for that piece, waterfall you do all of step 1, step 2, etc.
22. What is the difference between `#new` and `#create`?
Create: creates a new instance and saves it, New: only creates a new instance
=======
11. What is CRUD and why is it important?
12. What does HTTP stand for? 
13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
14. What's an ORM?
15. What's the most commonly used ORM in ruby (Sinatra & Rails)?
16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
17. What's a migration? 
18. When you create a migration, does it automatically modify your database?
19. How does a model relate to a database?
20. What is the difference between `#new` and `#create`?

Review Questions:  
21. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  
22. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone'],
  brunch: {cost: $35, supplies: ['mimosa flutes'],
  antiquing: {cost: $200, supplies: ['list of antique stores'] 
}
```
How would I add 'granola bar' to things you should have when hiking?
23. What are the 4 Principles of OOP? Give a one sentence explanation of each.
>>>>>>> 2fb14b2e0e3ed48c9764bf58cbb7e1fedd592c5b
