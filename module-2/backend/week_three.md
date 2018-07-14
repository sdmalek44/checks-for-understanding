## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?  
`rails new -T -d="postgresql" --skip-turbolinks --skip-spring` 

2. What do Models generally inherit from in rails?  
`models inherit from ApplicationRecord which inherits from ActiveRecord::Base`

3. What do Controllers generally inherit from in a rails project?  
`controllers inherit from ApplicationController which inherits from ActionController::Base`

4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?  

`config/routes.rb` 
```ruby
Rails.application.routes.draw do  
  resources :horses, only: [:show]  
end
``` 

5. What rake task is useful when looking at routes, and what information does it give you?  
`$ rails routes`  

6. What is an example of a route helper? When would you use them?  
An example of a route helper is instead of typing `'/horse/3'` to get to the horse three show page you would type  
`horse_path(horse)` if `horse` in the parenthesis was an instance of that specific horse.  

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?  
`_path` returns a relative uri while `_url` returns an absolute uri.  

8. What are strong params and why are they necessary?  
Strong params are where you make a method that modifies the params in the controller to only pass in things that you need and ignore others.  

9. What role does `form_for` play in helping us create our forms?  
`form for` allows us to easily make forms that can be specific to creating or updating a resource. You tell it what resource you are working with and what information it will take in and it updates the params accordingly once the submit button is pressed.  
10. How does `form_for` know where to submit the user's input?  
`form_for` knows where to submit the users input when you tell it what resource it is working with. It will create the path according to what you give it.  

11. Create a form using a `form_for` helper to create a new `Horse`.  
```ruby
<%= form_for @horse do |f| %>  
<%= f.label :name %>  
<%= f.text_field :name %>  
<%= f.submit %>
<% end %>  
```  

12. Why do we want to validate our models?  
We want to validate to make sure a resource can not be created or updated without giving it the attributes it needs.  

13. What are the steps of the DNS lookup?  
The first step is the user enters a url into their browser. It first asks the resolving name server if it knows what the IP address is. The resolving name server asks the root server. The root server will give the correct TLD server to check. The resolving name server will then check that Top Level Domain server. The TLD server will give the resolving name server the right authoritative domain server to check. The resolving name server will check that domain server. The authoritative domain server should return the correct IP address for that URL. The resolving name server will take that information and give it back to the client for the client to make the request.  

### Review Questions
14. How would you call the method `prance` from within the method `move` on a `Horse` instance?  
```ruby
def move 
  prance 
end 
```

15. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?  
to return true `furniture[:purchased]` and to return 3 `furniture[:table][:height]`  

16. What is inheritance?  
Inheritance is when methods are inherited by one class from another class.  

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week
