## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!).

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
Active Record is an ORM 'system-?', which allows you to connect databases to control systems to maximize efficiency when interacting with a CRUD system - creating, reading, destroying, or updating information in that database

2. Assume you have the following model:
```ruby
class Team << ActiveRecord::Base
  def self.highest_number_of_players
  end
  def self.highest_number_of_players_team_name
  end
  def self.highest_score_in_season
  end
  def self.highest_score_in_season_team_name
  end
  def self.most_common_jersey_color
  end
  def self.least_common_jersey_color
  end
end
```
What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
**see above**

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?
Team.find(4).name
team = Team.find(4).owner_id
Owner.find(team)
**OR** Owner.find(Team.find(4).owner_id)

4. Assume that you added a line to your `Team` class as follows:
```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```
Now how would you find the owner of the team with an id of 4?
Team.find(4).owner_name

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? **Draw the schema diagram.** - ? draw? I can create the relationships...
college -> many(teachers) to many(students)
teacher
has_many :students
student
has_many :teachers

elementary -> one(teacher) to many(students)
teacher
has_many :students
student
belongs_to :teacher


6. Define foreign key, primary key, and schema.
foreign key - the named id (with a direct relationship to the primary key) LINKED to the primary key
primary key - the incrementing id on one table
schema - relationship between the two

7. Describe the relationship between a foreign key on one table and a primary key on another table.
the foreign key is expands on the primary key, in another table
for example: primary key: id in the owner table; foreign key: owner_id in the team table

8. What are the parts of an HTTP response?
a header and body

### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
.where - locates instances according to a specification (can be used on a collection)
.find - locates an instance according to the id
.find_by - locates an instance that meets the set params
.create - new AND save in one neat little package
.group(:).count - get the total of grouped items in one go (pretty handy when paired with min/max)


2. Name your three favorite ActiveRecord rake tasks and describe what they do.
rake db:rollback - rolls a migration back so you can fix it, then you can choose to migrate again after making the changes
rake db:migrate - defines and creates a table
rake db:create - creates a database

3. What two columns does `t.timestamps null: false` create in our database?
updated_at
created_at

4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
one (school) to many (teachers)

5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
school
has_many :teachers
teacher
belongs_to :school

6. Give an example of when you might want to store information besides ids on a join table.

7. Describe and diagram the relationship between patients and doctors.
hospital - many(doctors) to many(patients-patients often have more than one dr in hospitals)
doctor
has_many :patients
patient
has_many :doctors

dental/private practice/small clinic - one(doctor) to many(patients)
doctor
has_many :patients
patient
belongs_to :doctor

8. Describe and diagram the relationship between museums and original_paintings.
on one particular date: one(museum) to many(original_paintings)
museum
has_many :paintings
painting
belongs_to :museum

**BUT**
over the course of a year: many(museums) to many(original_paintings)
because paintings rotate between museums when out on tour
museum
has_many :paintings
painting
has_many :museums

9. What could you see in your code that would make you think you might want to create a partial?
redundancy w/in the views - new and edit, in particular
