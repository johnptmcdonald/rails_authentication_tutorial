# Rails Authentication Tutorial

This is a run through of a basic authentication (signup/login) system in Rails. I am using ruby version 2.1.2p95 and Rails 4.2.0

### The User model
We need to create a User model in order to be able to store our users in the database.

When a user signs up we are going to ask him for a name, email, password, and password_confirmation.

However, we CANNOT save the password in plain text in the database! If anyone gained access to our database, they would have everybody's password. We need to save an _encrypted_ version of the password. By convention, we call this encrypted version the _password_digest_.

So let's create our User model:

```ruby
rails g model User name email password_digest
```

This will create three string fields for our User model in the database. 

