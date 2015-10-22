Lecture 8: Idea to App
=====

This week, we take an idea and turn it into an app.
You can see the changes made in code for every step in the lecture
notes as follows:

Initial app - https://github.com/rails-decal/fa15-lecture7

------

Step 1: User/Post models
-----

```ruby
rails generate model User
rails g model Quit # g is an alias for generate
# Edit migration files
rake db:migrate
annotate # Generates helpful schema info in model files
```
[**Step 1 Code**](https://github.com/rails-decal/fa15-lecture7/commit/57308dfd12d505e2a072bfd437865f3a696d8805)

------

Step 2: User auth
-----

```ruby
gem 'devise' # In Gemfile, not typed in terminal
bundle install
rails generate devise:install
rails generate devise User
rake db:migrate
annotate
```
[**Step 2 Code**](https://github.com/rails-decal/fa15-lecture7/commit/e99cf9875e7e81f2fc0c85b0a5030f6fdbe64324)

------

Step 3: Validations + Associations
-----

```ruby
# Add validations
rails g migration AddUserIdToQuits
# Edit migration
rake db:migrate
annotate
# Add validation for user_id
```
[**Step 3 Code**](https://github.com/rails-decal/fa15-lecture7/commit/5e4e1e7de1c262820d54014935c3585e9ffdbe7c)

------

Step 4: Seeds, routes, user show, user index
-----

```ruby
# Add routes
rake routes # To review the routes you made
# Make app/controllers/users_controller.rb, app/views/users/show.html.erb
# Edit db/seeds.rb
rake db:setup
```
[**Step 4 Code**](https://github.com/rails-decal/fa15-lecture7/commit/7429c5e1a19e6747a7b3b1e5da2ae714e98e3ecf)

------

Step 5: Edit, update Quit
-----

[**Step 5 Code**](https://github.com/rails-decal/fa15-lecture7/commit/8a4f4758fbea6474e0f4fb8c4e3437ab11b18dea)

------

Step 6: New, create Quit
-----

[**Step 6 Code**](https://github.com/rails-decal/fa15-lecture7/commit/da11ef12a55763d719c80a5dd54198096d84c98e)
