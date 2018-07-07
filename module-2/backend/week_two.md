## Week Two - Module 2 Recap

Fork or re-pull this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR.


### Week 2 Questions

1. At a high level, what is ActiveRecord? What does it do/allow you to do?  
ActiveRecord is a way to do object relational mapping. It allows us to calculate data logic easily with built in methods. It allows us to use built in methods rather than raw sql to access things that we need from the database.   

2. Assume you have the following model: 

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?  
You can call Team.create(name: 'cougars') to create a new object. Team.where(name: 'cougars) to search for all teams with the name 'cougars'. We have methods like these because they are built in with active record.  

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?  
`team = Team.find(4)`
`Owner.find(team.owner_id)`  

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```  

Now how would you find the owner of the team with an id of 4?  
`team = Team.find(4)`
`team.owner`  

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.  
-many to many  
https://imgur.com/HLSu65l

6. Define foreign key, primary key, and schema.  
A foreign key is a key that relates to the primary key of another table. It allows you to link tables together to get what you want out of them.  Primary key is usually the id that your table automatically gives the rows as resources are created. A schema is a blueprint for all of the tables in your database. 

7. Describe the relationship between a foreign key on one table and a primary key on another table.  
A foreign key on one table can correspond to the primary key on another table which allows you to link the two tables together. The foreign key belongs to the corresponding primary key table.  

8. What are the parts of an HTTP response?  
The http response has a status line with a status code and reason phrase. It also has headers and a body.


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.  
.order, .where, .find, .group, .average  

2. Name your three favorite ActiveRecord rake tasks and describe what they do.  
`$rake db:{drop,create,seed}`  

3. What two columns does `t.timestamps null: false` create in our database?  
created_at, and updated_at  

4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?  
one to many. a school has many teachers.  

5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?  
you will need to put a belongs_to :school in the teacher class and a has_many :teachers in the school class.  

6. Give an example of when you might want to store information besides ids on a join table.  
if you had invoice items with an invoice id and an item id but you also wanted invoice items to have a quantity and price.

7. Describe and diagram the relationship between patients and doctors.  
patients have one doctor. doctors have many patients. one to many . 

8. Describe and diagram the relationship between museums and original_paintings.  
one to many. museum could have many original_paintings but an original painting can only have one museum cause there is only one original.  

9. What could you see in your code that would make you think you might want to create a partial?  
if you were repeating a lot of the exact same html you would want to make a partial.  


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week
