## Week Three - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR.

1. At a high level, what is Node?

- Node is a Javascript that is capable of being written and run in a server environment.

2. What is Express? What is Express similar to in the Ruby world?

- Express is a framework that allows Node written applications to be used as web applications.

3. How do we setup a route when creating an API with Node and Express? Please provide a code snippet.

- The app (which is set to express along with other uses of functions) is set. The route is then set using the app. For example, a GET to a "Jobs" route would look like:

```
app.get('/jobs', callbackfunction() {})
```

4. What do we use Knex for?

- Knex is used to connect server-side Node code to a database.

5. How could you organize your code to follow the MVC design pattern in your Quantified Self project?

- The Server.js file can be used as the controller/routes. Server.js would house the actual route definitions (GET, POST, etc.). A separate folder containing database queries for given resources can be used as the "Models". Views are handled by the front end AJAX and API calls. However, we could house those in a views subdirectory should we want to pull the two applications together.

6. How do you execute raw SQL in node?

- Use database.raw('SUPER AWESOME sql CODE goes HERE')

7. What are some advantages to having your front end and back end code live in separate applications? What are some disadvantages?

- This is a tough one...

- Advantages: Since all code lives in same application, theoretically, the communication between the front and back end would be faster than if they were housed on separate servers.

- Disadvantages: Intertwining the code could get messy. A small "fix" on the back end could break the front end (vs just not send the correct data should the applications live separately.)

#### Review  

8. Describe DNS.

- Domain Name Servers. DNS allows the navigation and look-up of websites by name (www.google.com) to be translated to the hardcoded IP address of that named website (i.e. 192.168.0.1).

9. What does writing clean code mean to you?

- Writing clean code means readable, well-factored, reusable and not "esoteric", for lack of a better term. It needs to have potential future use for later development.

10. If you were building an application that models hotels, what classes would you need? What classes would be responsible for what functionality?

- Room: Bed, Shower, Layout, Size
- Floor: Consist of Rooms, Elevators, Layout, Size
- Person: Names, Type (worker vs. customer)
- Job: Job type, many persons
- Hotel: Consist of Floors, jobs, customer
- (This could be constructed in many different ways and at a lot of different levels of granularity)
