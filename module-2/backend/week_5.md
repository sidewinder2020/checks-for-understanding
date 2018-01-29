1. How do we make flash messages display on a page?
before an action in the controller, set a flash message [:key] and ="value"(msg)
then, in the application layouts (or a particular view, if you like) -
  <% flash.each do |name, msg| %>
    <div class="alert alert-success" role="alert"">
      <%= content_tag :div, raw(msg), class: name %>
    </div>
  <% end %>
(the div's seems a little redundant, but allow for better styling) - and the each allows for multiple flash messages to be displayed at one time, on one page

2. Where is cart information/temporary information usually stored?
session[:cart] - cart acts as the key to access that session's info - then it's stored as a hash (or that's how we have it set up)

3. What might be some reasons not to store cart in our database? Are there any reasons why we would want to persist that information?
I know I like to add things to my cart, then never checkout - this could easily fill up a database with orders that were never committed, and skew data for quarter reviews
Once an individual checks out, then you want to persist the data, even if the order is subsequently cancelled, because that is important info for the accounting department, or small business owner

4. What is the purpose of the asset pipeline?
to precompile assets and minify-? (take out whitespace/commas/etc.)

5. Why do we precompile our assets?
so that we don't have to do multiple requests for the same, unchanged, data - send it once, in a package, and be done with it

6. What do each of the following tags do?

```ruby
<%= stylesheet_link_tag "application" %>
go back to the stylesheet to grab information on how to style this particular piece

<%= javascript_include_tag "application" %>
include javascript on this particular piece, according to the javascript file in your project

<%= image_tag "rails.png" %>
allows you to display an image - acts as html's <img src=""> tag
```

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
version control
known conflicts
implementation

Our readme's allow future employers to look at our project, before cloning it down, and makes them much more likely to want to tinker around with it(if the instructions are good, and the premise looks interesting)

Also, if anyone else were to want to mess around with what we've built, updating as we go clues them into known issues, and solutions, and we're less likely to forget to include such information later on

8. What are the top four accessibility issues that we as developers should be aware of?

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
before_save is an example of a callback, we would find it in the model (where the method, being called, is written)

10. Given the following object, how would we create a scope for all users who are active?

```ruby
User.create(name: "Happy", active: true)
```

  class User < ActiveRecord::Base
    scope :true, -> { where(active: 'true') }
  end

OR  

  def self.true
    where(active: 'true')
  end

11. What is the difference between a scope and a class method?
a class method has to be called and can be almost anythign, but a scope is mainly used to narrow the database - ? maybe...
