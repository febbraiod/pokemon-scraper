##Objectives:
1. Set up a `SQLite` database
2. Scrape and save data into your database
3. Use data to make ruby objects

###Overview
In this lab you will set up your schema, scrape data, insert it into your db and then build out methods to manipulate your data.

For our purposes the `Pokemon` class is responsible for saving, adding, removing, or changing anything about each pokemon. Your scraper is not responsible for knowing anything about them.  

###Note
We have set up your scraper class for you, which you can see in `lib/scraper.rb`. We have also created a `schema_migration.sql` file that will run the `SQL` statement to set up your database in `db/pokemon.db`. Your only job is to build out the methods to save and find pokemon in the database.

###Create Our Pokemon Class
Our `Pokemon` class can be found in `lib/pokemon.rb`.
This is where you will build your methods.

###A Note On Inserting Into the Database
When you use sql to insert into a database you write out the values by hand and insert them into the database.  However, when you insert your pokemon into the database you don't want to insert them into the query via string interpolation because of potential [dangerous consequences](http://xkcd.com/327/).  Instead we need to [sanitize](http://stackoverflow.com/questions/9614236/escaping-strings-for-ruby-sqlite-insert) the data that goes into the query string you need to [execute](http://rdoc.info/github/luislavena/sqlite3-ruby).


###Getting Started
- Fork this repo, and clone your fork.
- `bundle install` (if that doesn't work run `bundle update`)
- Follow the pending RSPEC tests to get your sense of direction.

<a href='https://learn.co/lessons/pokemon-scraper' data-visibility='hidden'>View this lesson on Learn.co</a>
