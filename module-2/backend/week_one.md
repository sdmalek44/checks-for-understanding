## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.  
GET - is requesting to get content associated with a certain route and display that content in the browser.  
POST - is requesting to add an entirely new element to a page.  
PUT - is requesting to completely change an element on a page.  
PATCH - is requesting to change some parts of an element on the page.  
DELETE - is requesting to delete an element off of a page.  

2. What is Sinatra?  
Sinatra is a framework used with ruby to build web applications.

3. What is MVC?  
MVC is a way to structure your web application. It has a view which holds html and any display logic. It has a controller which handles any application logic. It also has a model which handles any data logic and has access to the database. 

4. Why do we follow conventions when creating our actions/path names in our Sinatra routes?  
We want to have restful applications which depend on the http verb and the route. The site also becomes more user friendly with routes that make sense.  

5. What types of variables are accessible in our view templates without explicitly passing them?  
We have access to instance variables or local variables that can be accessible in the view file without passing them. 

6. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?  
  
  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

7. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?  
erb :index, locals: {name: Mr. Ed}

8. What's the purpose of ERB?  
ERB allows you to use ruby code with html to display things in your view.

9. Why do I need a development AND test database?  
You need to constantly clean your database after every test and you wouldn't want to clean your development database everytime you ran a test. 

10. What is CRUD and why is it important?  
CRUD is an acronym for all of the basic functions we would like a dynamic application to have. We want it to be able to create, read, update, and destroy a resource.

11. What does HTTP stand for?  
Hypertext Transfer Protocol is a protocol we use while sending and recieving data packets over the web. 

12. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?  
`<% %>` and `<%= %>` are the two ways to interpolate ruby in an ERB view. The first one is if you want the ruby code to be hidden from the user. The second one is if you wanted to see the ruby code value in the view. 

13. What's an ORM? What does it do?  
ORM stands for object relational mapping. It is when an object model is used to represent a database. It allows you to access elements from a table as objects to relate tables to one another easily. 

14. What's the most commonly used ORM in ruby (Sinatra & Rails)?  
Active Record is the most commonly used ORM in ruby.

15. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.  
`get '/restaurants'` - used to access the page with all of the restaurants listed on it.  
`get '/restaurants/new'` - form to create a new restaurant and submit.  
`post '/restaurants'` - create a new restaurant in database.  
`get '/restaurants/:id'` - used to access a specific restaurant.  
`get '/restaurants/:id/edit'` - form where you enter the edit information and submit.  
`put '/restaurants/:id` - update the restaurant and display updated restaurant.  
`delete '/restaurants/:id'` - delete a specific restaurant.  

16. What's a migration?  
A migration is how you set up the attributes you want your table to have.

17. When you create a migration, does it automatically modify your database?  
No, it only allows you to set up how you want your table to be, not actually create it. rake db:migrate creates it using your migration file that you made. 

18. How does a model relate to a database?  
A model relates to a database by using an ORM such as Active Record. It allows you work with objects to manipulate your database.

19. What is the difference between `#new` and `#create`?  
`#new` is a class method that creates a new instance of a class. `#create` is a class method provided by active record that both creates a new instance and saves it into the database.


### Review Questions:  
20. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  
`CSV.open("films.csv", headers: true, header_converters: :symbol).each {|row| Film.create(row.to_h)}`

21. Given the following hash:  

```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone']},
  brunch: {cost: $35, supplies: ['mimosa flutes']},
  antiquing: {cost: $200, supplies: ['list of antique stores']}
}
```
How would I add 'granola bar' to things you should have when hiking?  
`activities[:hiking][:supplies] = 'granola bar'`

22. What are the 4 Principles of OOP? Give a one sentence explanation of each.  
abstraction - one class should not need to know about the inner workings of another just to use it.  
encapsulation - hiding data implementation by restricting access to public methods.  
inheritance - reusing code of existing superclasses.  
polymorphism - ability of a language to process objects differently depending on their data type or class.  


### Self Assessment:
Choose One: (erase the others)
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week
