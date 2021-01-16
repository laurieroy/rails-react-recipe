# Recipe

This follows a [digital ocean](https://www.digitalocean.com/community/tutorials/how-to-set-up-a-ruby-on-rails-project-with-a-react-frontend) 
tutorial on creating a Rails app with a React front end, by Chuks Opia. Postgres is dev and prod db. The project is a collection of recipes, where the user can View, Create and Delete recipes. Styling is with Bootstrap 4.

It is built with Ruby 2.6.3 on Rails 5.2.3 on a mac, browser tested on safari and chrome

## Steps Followed
*  Have or follow instructions (I've provided the link to macOS) to install the following apps:

* [node.js and npm](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-and-create-a-local-development-environment-on-macos) installed on your machine
* [Yarn](https://classic.yarnpkg.com/en/docs/install#mac-stable) package manger to download React
* [Ruby on Rails](https://www.digitalocean.com/community/tutorials/how-to-install-ruby-on-rails-with-rbenv-on-macos)
* [PostgreSQL](https://www.digitalocean.com/community/tutorials/how-to-use-postgresql-with-your-ruby-on-rails-application-on-macos) Follow steps 1 and 2. 
* Create new rails app specifying to use postgres for the db, and webpack bundler for React and rails version 5.2.3
* Configure the config/database.yml file for the user role and db specified in setup
* Install React Router, Bootstrap, jQuery and Popper for the front-end
* Set up the Homepage index as root route
* Configure Rails to use React for the front-end
* Add Recipe, controller and model, requiring name, ingredients and instruction
* Build out Index, Create, Show, Delete routes and views

## To Run App on your local machine:

From the terminal: Clone the repo and change to that directory:
```
$ git clone https://github.com/laurieroy/rails-react-recipe
```

Install the gems locally:
```
$ bundle install
```

Create databases: 
```
$ rails db:create
```
(builds a development and testing database)

Run migrations:
```
$ rails db:migrate
```

Seed database with initial 9 recipes: (optional). It runs the code found in `~/rails_react_recipe/db/seeds.rb`.
```
$ rails db:seed
```


## Run
To run your server locally
```
$ rails s
```

By default the application will listen on port 3000. Nav to http://localhost:3000 to see the app in the browser.

To shut down the server use `Ctrl-C`

### TODO:

 I plan to add in the following functionality:

 * User login
 * Admin role
 * Edit recipe
 * Verify delete
 * Add Comments
 * Upload photos 