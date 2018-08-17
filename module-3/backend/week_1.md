## Week One - Module 3

Some of these questions are from this week, some are from previous weeks, and some are new concepts. Try answering without research first. If you are not sure, take a guess but acknowledge that it's a guess (faking an answer in an interview without acknowledging it as a guess is a bad idea). Follow up with the necessary research to understand these concepts. These tend to be common themes during the job hunt and are worth having a solid understanding of.

1. What is `json`, what does it stand for, and why is it important?  
Json stands for javascript object notation. It can be used to convert data from an api into an ruby object. Human readable and machine readable.  

1. What kind of object is JSON in Ruby? How do we know it's JSON?  
The json file comes in as a string in ruby. `JSON.parse()` turns json data into a hash. We know it is JSON because it contains keys with double quotes followed by a colon.  

1. What's an API?  
API stands for application programming interface. It is a way of presenting data in a notation that is easily converted into many different programming languages and pulled into a database.  

1. What's a RESTful API? How does that look in Rails?  
A restful API is one that follows typical route and controller conventions. In rails your controllers should only contain the conventional crud methods(show,index,create,update, etc.). The api should try to use the traditional route and namespacing conventions as much as possible.  

1. What is an ORM, what does it stand for, and why is it helpful?  
It stands for object relational model. It is helpful for converting rows in a database table to objects in a programming language like ruby. Active Record is an ORM used for converting table rows to objects in ruby.  

1. How do you create a record in the following table in SQL? In Active Record?   
   (Users table with columns first_name, last_name, email, and age)  
   SQL:
   ```
   INSERT INTO users (first_name, last_name, email, age) 
   VALUES ('Bill', 'Billerson', 'bill@bill.bill', 31)  
   ``` 
   Active Record:  
   ```  
   User.create(first_name: 'bill', last_name: 'billerson', email: 'bill@bill.bill', age: 31)  
   ```  
   
1. How would you refactor this method?

```
def people_with_brown_hair
  people_with_brown_hair = []

  people.each do |person|
    if person.hair_color == "brown"
      people_with_brown_hair << person
    end
  end

  people_with_brown_hair
end
```  
Using Active Record:  
```  
def people_with_brown_hair 
   People.where(hair_color: 'brown')  
end  
```  

1. Given an array numbers = [1,2,3,4,5], find the sum of the doubles of all the numbers.  
`numbers.inject(0) {|collector, number| collector += 2 * number }`  


#### Self Assessment  
Rate yourself on the following scale.  
4  I know and understand all these concepts and did not have to look anything up  

^^ Please let an instructor know where you'd like support to catch you up.
