# Rails Commands Quiz

Fork, clone, and write your answers directly in this file. Then submit a pull request.

### Question 1

I want to start a new Rails project/app called `BunnyApp`. What command should I type in the terminal?

mkdir BunnyApp
cd BunnyApp
rails new . -d postgresql

### Question 2

I want to create a new model called `Bunny`, with the following attributes: name (string), color (string), and age (integer). What command(s) should I type in the terminal and/or Sublime? (In your answer, create both a migration and the model file.)

rails g scaffold Bunny name:string color:string age:integer
rails db:create db:migrate db:seed

class Bunny < ApplicationRecord
end .......should already be filled in

### Question 3

What does the command in Question 2 do, exactly? What files are created, where are they located, and what does the database look like at this time? Explain.

g is generate
scaffold is many of the directories we may need, properly named for us
also much of the code for forms and relationships and paths is done for us
Bunny is now a class and I created an empty table in postgresql with 3 columns

### Question 4 ######

I want to create a database and make it reflect the new model I created in Question 2. What command(s) should I type in the terminal?

I don't know the answer.  I thought that's what I did in Question 2.
I would guess the db:d, c, m, s commands but am I wrong?

### Question 5 ######

I want to look at the actual database that has been created. What command should I type in the terminal?
psql
\l
SELECT * FROM bunny;  didn't work, I don't know this either.
### Question 6

I want to see a list of all the URLs available in my app, along with the HTTP requests and controllers associated with them. What command should I type in the terminal?

rails routes or rake routes should work

### Question 7

What line should I add to `config/routes.rb` to create a complete set of RESTful routes for a "bunnies" resource?

resources :bunnies

### Question 8

According to standard Rails conventions, what directory and filename would the BunniesController be located in, starting from the root of the project?

bunny/app/controllers/bunnies_controller.rb

### Question 9

According to standard Rails conventions, what directory and filename would the "show" view for bunnies be located in, starting from the root of the project?

bunny/app/views/bunnies/show.html.erb

### Question 10

I have worked on my app and finally want to see it in action. What command should I type in the terminal, and where should I navigate to in my browser?

rails s
localhost:3000
