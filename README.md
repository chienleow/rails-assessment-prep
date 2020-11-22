# Rails Assessment Prep 👨🏻‍💻 👩🏻‍💻

## 1. Difference between Render and Redirect
* Resources: [Rendering & Redirecting](https://www.theodinproject.com/courses/ruby-on-rails/lessons/controllers#rendering-and-redirecting)
* Render tells Rails which view or asset to show a user, without losing access to any variables defined in the controller action.
* The redirect_to method tells your browser to send a request to another URL. Since the request is completely different, the view to which you redirect will NOT have access to any variables defined in the controller.
## 2. Password
* Rails Authentication [Video example (timecode 4:40)](https://www.youtube.com/watch?v=4O_kCICoebA)
* `has_secure_password` gives us the .authenticate method in our Controller, what encrypts our password when we pass it in our password column, in table called `password_digest` 
* How does `password_digest` work? Original password is NEVER saved, bcrypt encrypted the password for us before saving it in the database
* Explain `bcrypt`: `bcrypt` salt and hash password, encrypt our password 
## 3. Scope Method *(Important)*
* [Ruby Guides](https://www.rubyguides.com/2019/10/scopes-in-ruby-on-rails): When to use Scope, Scope VS Class Method
* Active Record Scope Methods [(Seth @ Flatiron) 34mins](https://www.youtube.com/watch?v=akwUv3KzRcc)
* **What is scope method?** Class level methods that limit your return to be a scope return.
* Scopes are custom queries that you define inside your Rails models with the scope method.
* When working on scope method, look at schema, the attributes are the ones we have opportunity to work from
* [API DOC: ActiveRecord::Scoping::Named::ClassMethods](https://api.rubyonrails.org/classes/ActiveRecord/Scoping/Named/ClassMethods.html)
* **Question: Difference between scope method and class method**
* [(Medium) How is a scope different from a class method?](https://medium.com/le-wagon/what-are-named-scopes-and-how-to-use-them-rails-5-5a0444d8b759)
	*  **Chaining** - it will not return `nil` but rather an empty array
	* **Readability** - Scopes can be written in just one line, great way to keep your model dry
## 4. Separations of concerns 
* Don't call database from View
* Think MVC

# Notes from Assessments
1. Walk-through Google OmniAuth in browser, in code
	- Refactored `google_login` method
2. Walk-through "Sign in" in browser, in code
3. Explain `@user.authenticate`, why wouldn't `@user.password_digest` work? Refer to Password notes above. 
4. Show how the join table happens, the many-to-many relationship in browser and in code
5. Refactored `current_user` helper method, read more on `=||` or equals ruby [(stackoverflow)](https://stackoverflow.com/questions/995593/what-does-or-equals-mean-in-ruby), don't call database too often, only call it when you need it, now your app is small, but when you have  a lot of users in database, it might slows you down if you keep calling database
6. Show Scope method in browser and in the code
	- Explain the difference between using Scope Method or using Class Method with the scope, there is no real big difference, but using scope has its advantage in terms of organization, easier to spot it when you have a lot of Class Methods and Scope Methods in your app, Scope Method would return empty `activerecord:relation`
7. Nested routes and live coding (do scope, where)
8. Live coding question: "find username using scope"
9. Live coding question: "find the team with the most users"
	- Use join in scope, joining two tables first, [(stackoverflow)](https://stackoverflow.com/questions/16996618/rails-order-by-results-count-of-has-many-association)
	
## Live Coding Tips:
Steps I took:
1. Ask more clarifying questions if needed (it helps make you less nervous)
2. pull out your notes to pseudo code first (write down what the instructions were)
3. Talk your thoughts out loud throughout the whole process
4. You can google!! (only refer to ruby guides, api docs etc, no stackoverflow)

## Mindset shift:
1. Relax, think of the instructor as your pair programming buddy
2. "What can I learn from this review? What can I learn from this live coding session?"

