## Week Four Recap

### Instructions
Fork this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

* What is a cookie?
  * Cookies are hash-like objects that are maintained browser-level until their specified expiration date.
* What’s the difference between a session and a cookie?
  * A session is a more secure cookie.
* What’s a flash and when do you want to use flashes?
  * A flash is a temporary message that can be useful for error or success messages.
* Why do people say “HTTP is stateless”?
  * On their own, HTTP requests do not save any information after they have been made.
* What’s authentication? Explain.
  * Authentication is the process of verifying that a user is registered (stored in the db) with an app, allowing them to log into the app, and storing their user info into a session until they opt to logout (or the session expires).
* What’s the difference between authentication and authorization?
  * Authentication is the process of checking if a user's information is stored in the database so that they can log in or log out of an application. Authorization is then determining the level of access a particular user has (aka what views or features they have access to based on role).
* What’s a before filter?
  * It's an action that will run before every controller method specified. Can be used to check if a certain user role is allowed to access a route/page.
* How do we keep track of a user once they’ve logged in?
  * You store a unique identifier (usually something like their user id) in a session. This session generally stays the same until the user opts to log out and end the session (or clear their user id from the session).
* When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
  * You'd namespace a resource when top level does not actually need to be it's own entity or resource. An Admin is a common example--an admin is just a user object with more clearance, so it doesn't need it's own model. Nested resources are when you need one entity to "own" another--for example, users could have multiple photos associated with their account.
* At a high level, what tools can you use to implement authorization? How would you use them?
  * Before filters can be used to implement authorization. There could be a method run before every action in an Admin::BlankController, for example, that checks to see if the user currently trying to access something has the role of "admin" or not.
* What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
 * From my understanding, it can associate a string value to an integer (which means the datatype in your db needs to be an integer as well). You declare the enum within your model.
* What are some strategies you can use to keep your views DRY?
  * Using helper methods and partials are two great ways to keep your views free from repition.
