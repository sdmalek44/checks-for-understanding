## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?  
It's a place where information is stored in the browser and can be used for future visits to a web address.  

2. What’s the difference between a session and a cookie?  
Cookies can only be stored on the client side where sessions can be stored client side and server side.  

3. What’s a flash and when do you want to use flashes?  
A flash is a message that will pop up on the page after you've done some action like creating a user or it could be a prompt telling you that you entered in the wrong information.  

4. Why do people say “HTTP is stateless”?  
It means the connection between the server and the browser is lost once the request response transaction ends.  

5. What’s authentication? Explain.  
Authentication defines which user is using the site. It requires you to enter usually a username / email and password to sign into a website.  

6. What’s the difference between authentication and authorization?  
Authentication is defining who the user is and authorization determines what parts of the site the user is allowed to go to.  

7. What’s a before filter?  
A before filter is a check to see if the user has authentication to visit a page before they are provided with the resource. Usually it will return some page not found message if they are not allowed to be there.  

8. How do we keep track of a user once they’ve logged in?  
Once a user has logged in we track a user by keeping some information like the users id in the session. We can also have a method that tries to find the current user and return that user object when called or nil if there is no current session.  

9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?  
You want to nest a resource when you want one resource to be created through another resource. When you use namespace it changes the path, the path helper, and will need to be accessed through a controller that is nested within another folder.  

10. At a high level, what tools can you use to implement authorization? How would you use them?  
You can first create a namespace that allows some resources to be accessed through another controller. You can put logic in your views for buttons that access these pages. You can also do a before filter in your nested controller so that if the user is not authorized to be there it will render a page telling them the resource doesn't exist.  

11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?  
An enum will take a number passed in as an attribute and assign it a string so that everytime that attribute is called it will return that string.  

12. What are some strategies you can use to keep your views DRY?  
A good strategy to DRY up your views is to use partials when you are using a lot of the same html. And putting things in your application.html file so they will show up in all of your views.  

### Reviews Questions 
13. Given the following array of hashes, how would I print an alphabetical list of holidays?  

```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]}},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]}},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}}
]
```  
`given.map {|hash| hash[:holiday][:name] }.sort` 


14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300?  
You could do .delete("$") on the string and then do .to_i on the string to change it to an integer.  


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week
