### Week 5 Questions

Re-pull from this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

### Week 5 Questions
1. How do we make flash messages display on a page?  
We assign a message like `flash[:notice] = 'this is a message` in the controller and then call the `flash[:notice]` in the view. 

2. Where is cart information/temporary information usually stored?  
It is stored in the session like `session[:cart]` and it can hold a hash of item ids as the keys and quantity of that item as the value. 

3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?  
If we wanted a user to be able to add things to a cart without being logged in and then log in to checkout the cart we could store the cart info in the session.  

4. What is the purpose of the asset pipeline?  
The purpose of the asset pipeline is to provide a framework to concatenate, minify, precompile and fingerprint JavaScript and CSS assets.

5. Why do we precompile our assets?  
Precompiling assets allows us to write in languages related to css/javascript.  

6. What do each of the following tags do?

```ruby 
<%= stylesheet_link_tag "application" %>
<%= javascript_include_tag "application" %>
<%= image_tag "rails.png" %>
```  
The first tag links the css stylesheet application.css. The second includes the javascript file application.js. The third one displays an image located in the assets images.  

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?  It is good to have a setup portion to tell the viewer all the steps they need to get your repo onto their computer and use it. The benefits of having a readme is that employers will go to it and know exactly why and how you did the work you did. That way they can make a better evaluation on whether they should hire you or not.  

8. What are the top four accessibility issues that we as developers should be aware of?  
The content should be percievable, operable, understandable, and robust(can be consumed by a wide variety of browsers).  

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?  
`before_save` is an example of a callback. You can use `before_save` to generate a slug.  

10. Given the following object, how would we create a scope for all users who are active?

```ruby 
User.create(name: "Happy", active: true)
``` 
```ruby
scope :user, where(active: true)
```

11. What is the difference between a scope and a class method?  
A scope is basically a class method that acts as a query builder. A class method can do other things than just that. 


### Review Questions:  
12. Given the following hash:  

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```  

  12a. How would you add item with id of 48 with a quantity of 4?  
  `given[:cart]["48"] = 4`  
  
  12b. How would you increase the quantity of item 29?  
  `given[:cart]["29"] += 1`  
  
  12c. How would you find out how many items your user is thinking about purchasing?  
  `given[:cart].values.sum`  
  
13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?  
Polymorphism means a subclass can override a method of the base class. Duck typing means code will accept any object that has a particular method.  

14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  
```ruby
given.gsub!(/[)-]/, '.').delete("(")  
```


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week
