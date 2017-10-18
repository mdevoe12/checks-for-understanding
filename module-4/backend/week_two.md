## Week Two - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What is Webpack and why is it useful?
  -Webpack bundles files and modules together so as to be used in your development (...maybe production?) environment.

2. When do you want to use event delegation?
  -Event Delegation can be used to target a higher element on the DOM than the element that was selected.
  
3. What's one difference between ES5 and ES6?
  -One difference would be how variables are declared. ES5 uses "var" to declare variables, whereas ES6 uses both "let" and "const" for variable definitions.

4. How are you using the MVC design pattern in your Quantified Self project?
  -Currently, we have just the views operating in Javascript. The views make calls to an API that is currently in a Rails environment (with the model and controller layers currently defined). Moving forward with Express, we'll be structuring our files, manually, to have the "models" built out with SQL queries, the server.js file will act like routes.rb and we'll have separate namespaced controllers to handle foods and meals.

5. How do you execute raw SQL in node?
  -I believe this is done using a .raw() function.

6. What's a callback function and what are some reasons when we use/need callback functions?
  -Callback functions are passed inside of a parent(?) function to perform an action further down in the parent function.

7. What is CORS?
  -I have absoluletely no idea...looking this up.

8. What are some steps to avoid CORS?

#### Review  

9. Why do people say "HTTP is stateless"?
  - HTTP is stateless in that "state" is not transferred between requests. Information is sent and any type of "state" would be stored in cookies.

10. What is a RESTful API?
  -RESTful APIs follow the standard RESTful request verbs in order to transfer information via HTTP. These verbs include GET, PUT, PATCH, DELETE.

11. What are some main characteristics of a team following an agile workflow?
  -Short sprints (2 - 4 weeks), the ability to pivot on projects quickly, no long term planning (in that there will not be a set timeframe for a feature release for 6 months out).

12. What are some advantages/disadvantages to using OAuth to authenticate a user?
  -Advantages: Outsource security to another company with more resources/security expertise. Less code and complexity inside your application.
  
  -Disadvantages: The information/security is outsourced. You/your team does not have immediate access for login issues or privacy concerns.
