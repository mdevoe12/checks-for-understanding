## Week One - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's the most useful thing you learned from completing the intermission week work?
  -General syntax and structure of Javascript. 

2. What are some tools to help debug JavaScript code?
  -Chrome Dev Tools
  -debugger
  -console.log(thing)

3. What are some tools you need in order to unit test your JavaScript?
  -npm
  -mocha
  -chai

4. What is the syntax for invoking a function?
  -functionName()

5. What's `this` in JavaScript?
  -'this' is a way of calling a particular 'thing' (for lack of a better term) on the page. 'This' could be an ajax call, an object, a tag or element. It depends on where 'this' is called.

6. What is Webpack and why is it useful?
  -Webpack bundles and readies javascript code (minifies and uglifies) for use in your development environment.

7. When/why do you want to use event delegation?
  -Event delegation can be used for targeting elements that may exist inside of parent elements. This is useful if you have multiple elements with the same name/id/class that exist in distinct parent elements.

8. What's `npm` and what do we use it for?
  -Node package manager. NPM can be used to run tests, install necessary node files to your project and ready a project for deployment.

#### Review  
9. What's the MVC design pattern? Describe each part of MVC.
  -M - Model: this is where a good chunk of the code/logic should live in your framework. Models contain resource information to be used and distributed. Models connect to the database.
  -V - Views: Views are the actual display pages of your site. Information is passed from the model through the controllers to the views.
  -C - Controller: Controllers are the traffic directors of the MVC system. Controllers send information to the appropriate model and/or view depending on the instructions.

10. What are a few ways to optimize a Rails application?
  -Caching
  -Indexing the database
  -Background workers
  -Message queues

11. What's a background worker? When would we want to use a background worker?
  -Background workers take the load off the rendering of pages and general system resources. Background workers allow you to queue information and run them at a designated time/or in a particular order.
