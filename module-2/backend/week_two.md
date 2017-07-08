## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?

  ActiveRecord sits allows ruby to communicate with a relational database. AR helps to map classes to table names, call specific methods instead of running complex SQL queries and interpret data from a SQL database into ruby type styling.

2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?

Methods - Team.all, Team.order, Team.find_by(name: "Team Awesome"), Team.where(location: "London")

While these methods aren't defined by the programmer, AR creates this methods upon the migration of the table in the databse and with the model creation (Team).

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?

Team.find(4).name & Team.find(4).owner_id (This wouldn't return the owner, just the primary key from the owner table).

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?

Team.find(4).owner.name

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.

Students and Teachers could have a one(Teachers)-to-many(Students) relationship or a many-to-many relationship.

Schema diagram for student-teacher join table -> http://imgur.com/a/XaGsZ

6. Define foreign key, primary key, and schema.

The primary key is the auto-incrementing 'id' column on a given table in a relational/sql database.
The foreign key is the primary key for a linked table that is stored in a separate column on a connected table (author_id in the books table).
The schema is the layout and directions used when a migration is run. The schema will list the tables, columns and format of those columns.

7. Describe the relationship between a foreign key on one table and a primary key on another table.

The foreign key is the primary key for a linked table that is stored in a separate column on a connected table (author_id in the books table).

8. What are the parts of an HTTP response?

Note - this is the only one I had to look-up as I could not remember:

Status Line, Header, Empty line, optional message body.


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.

  .find - Look-up by primary key. This is the fastest method for a record look-up.
  .where(column: "Search paramater") - Looks up all records that match a specific search parameter.
  .order(:column) - Orders search results based on a column argument (:name, :awesomeness_level, etc.) .order also takes additional arguments for ascending or descending order.
  .create - Create the thing! 
  .find_or_create_by - While this can run three potential SQL queries, therefore being potentially expensive, it allows you to find a specific thing, if it's not found, it will be created, if it isn't created it will be inserted into the appropriate table.

2. Name your three favorite ActiveRecord rake tasks and describe what they do.

rake db:test:prepare - I always forget to do this prior to running tests. It's slowly becoming my favorite because I desperately need it...

rake db:seed - Populate that database!

rake db:reset - I screwed up my development database. Time to remigrate and reseed.

3. What two columns does `t.timestamps null: false` create in our database?

created_at and updated_at

4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?


Students and Teachers could have a one(Teachers)-to-many(Students) relationship or a many-to-many relationship.

Schema diagram for student-teacher join table -> http://imgur.com/a/XaGsZ

5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?

Create a join table. 

class Student
has_many :teachers, through: :teacher_students
belongs_to :teacher

class Teacher
has_many :students, through: :teacher_students
belongs_to: student

class TeacherStudent
belongs_to :student
belongs_to :teacher

Schema diagram for student-teacher join table -> http://imgur.com/a/XaGsZ

6. Give an example of when you might want to store information besides ids on a join table.

...no idea...

7. Describe and diagram the relationship between patients and doctors.

Patients and doctors would have a many-to-many relationship. Patients can have many doctors (but not always) and doctors can have many patients.

8. Describe and diagram the relationship between museums and original_paintings.

This is a one-to-many relationship. Museums can have many original paintings, but original paintings don't have more than one museum at a given time.

9. What could you see in your code that would make you think you might want to create a partial?

If parts or all of a form are repeated. For example, edit and create often have the same field names.
