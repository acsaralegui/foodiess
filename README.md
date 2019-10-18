# README

# Foodiess
A Yelp clone that integrates with the Google Maps API and includes features like user comments, star ratings, image uploading, and user authentication.

# Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. First you have to set up a coding environment follow the link to install your coding environment https://github.com/university-bootcamp/coding-environment/blob/master/README.md#coding-environment-installation-guide 
Things you may want to cover:

* Ruby on Rails version

To set up your project, start by going to one of the terminals within your coding environment.
Remember, in these instructions, whenever you see a gray box with a dollar sign ($) at the beginning, type the command that follows it in a terminal window (following the dollar sign in that window). 1. Change to the directory where your code will be stored. $ cd /vagrant/src This will change your working directory to the folder where your code is. $ ls 3. Create a new application that uses postgres. Let's call this application splurty. 
$ rails new splurty --database=postgresql
4. Open your newly created splurty web application code in the Sublime Text editor. Open Sublime Text, click File > Open... (or File > Open Folder in Windows), and navigate to Desktop/vagrant/src/splurty.
5. Tell your Rails application how to connect to the database by editing the config/database.yml file. In Sublime Text, open database.yml and change it so it looks exactly like the code below:
default: &default
  adapter: postgresql
  encoding: unicode
  pool: <%= ENV.fetch("RAILS_MAX_THREADS") { 5 } %>
  username: postgres
  password: password
  host: localhost

development:
  <<: *default
  database: splurty_development
test:
  <<: *default
  database: splurty_test
production:
  <<: *default
  database: splurty_production
  # username: splurty
  # password: <%= ENV['SPLURTY_DATABASE_PASSWORD'] %> 
6. When you're done, save the file.
Start the Server
Now that you've configured database.yml and created your initial database, it's time to fire up the server.
Start the server by running the following command:
$ rails server -b 0.0.0.0 -p 3000


# Acknowledgments
University of Arizona coding bootcamp
