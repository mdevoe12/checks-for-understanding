## Week Four - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR.

1. What's your favorite project management tool?

Personally, I really like Pivotal Tracker. Pivotal's granularity and features makes it more robust and a better overall tool than Waffle. I enjoy being able to break individual feature stories/bugs/chores into sub tasks, use labels, create milestones/epics and estimate time.

2. Why do we create staging environments?

Staging environments are used for pre-production code. Final tests can be run. User acceptance can be gauged and any unknown bugs/behavior can (hopefully) be fleshed out prior to pushing the code to production.

3. What are the characteristics of a good README (in your opinion)?

A good README should communicate several core ideas:
-What the project/repo does or is meant for
-Languages and tools used to create the project
-What dependencies or items need to be used or installed prior to running the project
-Key information for interacting not only with the code, but with the development environment
-How to update the repo for a pull request or addressing a bug/issue

4. What's one main improvement you're going to make to your code regarding accessibility issues?

Well thought out color schemes. Millions of people are color blind. Poor color design can lead to difficulty in reading and accessing key information.

5. What are some basic security concerns to be aware of when building applications?

-Proper permissions: ensuring correct access is provided depending on user type. Closing open gaps in permissions is key as havoc can be wreaked otherwise.
-Proper encryption: using OAuth is all well and good. However, encrypting further session/access is important. Malevolent people may sniff packets and/or gain access to sensitive cookie/session data. Adding additional layers of security/encryption to the session process could be key in securing sensitive data.

6. Why is continuous integration helpful/important?

CI tests code in current environments to check for errors, failed tests or a variety of other undesired results that could break your production environment. This helps nip the potential issues in the bud and keeps the base branch/code in good working order.

7. What are some continuous integration tools?

-Travis CI
-Circle CI
-GitLab CI

#### Review  

8. What are some characteristics of "good" git workflow?

I believe good git workflow involves having a good system in place and following that system with rare exception.
For example:
-Master branch for pushing to staging/production
-Development branch being the primary foundation for any feature story branch (development is merged to master when a feature story is complete and ready for staging/production)
-Feature stories/bug fixes should be checked off of development with a consistent naming pattern (i.e. mhd_feature-add-user-show-page)
-Commits happen at least every 15 minutes/when a test passes/significant code is written
-Pull requests should be made back to the original brach it was checked off of (usually development). Pull requests should be detailed in nature (purpose of branch, what was done, potential issues). Another teammate should be tagged and that teammate (or others) should provide code review and merge into the base branch.

9. What are the four fundamental concepts of object oriented programming?

-Abstraction: Providing only essential information and "hiding" irrelevant details that allow for the essentials to be provided.
-Polymorphism: Allowing multiple behaviors to be present. For example: child classes/objects can use their behavior or a parents behavior.
-Inheritance: I often get this intertwined with polymorphism. Similar to the above, inheritance allows for objects/classes to pass/receive functionality from other classes.
-Encapsulation: Hiding unneeded information inside a class. For example: making sure methods are private so they cannot be run outside of the given class.

10. What's a module in Ruby and what's the difference between a class and a module?

A module contains constants, methods and code that can be used inside other files/classes/code in your application. Modules do not contain state or create instance variables while classes do.
