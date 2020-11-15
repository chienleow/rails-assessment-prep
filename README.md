# Rails Assessment Prep

## 1. Difference between Render and Redirect
* Resources: Rendering & Redirecting
* Render tells Rails which view or asset to show a user, without losing access to any variables defined in the controller action.
* The redirect_to method tells your browser to send a request to another URL. Since the request is completely different, the view to which you redirect will NOT have access to any variables defined in the controller.
## 2. Password
* Rails Authentication (timecode 4:40)
* has_secure_password gives us the .authenticate method in our Controller, what encrypts our password when we pass it in our password column, in table called password_digest 
* How does password_digest work? Original password is NEVER saved, bcrypt encrypted the password for us before saving it in the database
* Explain bcrypt: bcrypt salt and hash password, encrypt our password 
## 3. Scope Method (Important)
* Ruby Guides: When to use Scope, Scope VS Class Method
* Active Record Scope Methods (Seth @ Flatiron) 34mins
* What is scope method? Class level methods that limit your return to be a scope return.
* Scopes are custom queries that you define inside your Rails models with the scope method.
* When working on scope method, look at schema, the attributes are the ones we have opportunity to work from
* API DOC: ActiveRecord::Scoping::Named::ClassMethods
* Question: Difference between scope method and class method 
* (Medium) How is a scope different from a class method?
	*  Chaining - it will not return nil but rather an empty array
	* Readability - Scopes can be written in just one line, great way to keep your model dry
## 4.  Separations of concerns (Don't call database from View)
* Think Separations of concerns, MVC
