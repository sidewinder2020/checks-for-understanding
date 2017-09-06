## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?
rails new *program_name* -T --database=postgresql --skip-spring --skip-turbolinks

2. What do Models generally inherit from in rails?
ApplicationRecord

3. What do Controllers generally inherit from in a rails project?
ApplicationController

4. How would I create a route if I wanted to see a specific horse in my routes fitle assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
resources :horses, only: :index
(or put multiple routes in an array)

5. What rake task is useful when looking at routes, and what information does it give you?
rake routes - gives you the prefix(path), the url, and controller#action

6. What is an example of a route helper? When would you use them?
new_horse_path - use it in a redirect_to

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
a url is the url path in the web address, and the path is the helper used within rails for redirects/ link tos, etc

8. What are strong params and why are the necessary?
params.require(:blahblah).permit(:params, :params)
privatize the method AND reduce redundancy

9. What role does `form_for` play in helping us create our forms?
iterate through the object, set to the instance variable, and set the block variable to f (form)

10. How does `form_for` know where to submit the user's input?
In the controller, you set the instance variable (the form is assigned to), as well as the params when you are initiating the create (or new/save) method(s)

11. Create a form using a `form_for` helper to create a new `Horse`.
<%= form_for(@horse) do f %>
  <%= f.label :name %>
  <%= f.text_field :name %>

  <%= f.label :age %>
  <%= f.text_field :age %>

  <%= f.submit %>
<% end %>

12. Why do we want to validate our models?
it's the only thing client can access, so we want to be able to access it
