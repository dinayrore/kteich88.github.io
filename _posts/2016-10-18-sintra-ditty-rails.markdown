---
title: "Sinatra Doesn't Know That Ditty...Learning Rails!"
date: 2016-10-18
categories:
tags:
---

Yesterday was day one on learning rails, and all I can muster up, all I can fathom is _wow... what... magic!_ I thought the dark arts of JS was beyond comprehension, but Rails... I mean it literally populates a lot of the files and folders you need to create an app for you! Now that's magic! I do not have a complete comprehension of all things Rails, I don't even feel moderately comfortable with it as of yet. In fact I would feel more comfortable going back on stage with Sinatra, simply because I know all of the files and folders that I have created, and I created them myself, not by magic!

Another thought, why so many HTML pages? All of the apps I've developed with Sinatra are single pages with modals serving as additional "pages," which I thought made my app more functional, because then it does not send out so many requests to the server. ??? How do I dos? Also how can a Rails app also be an API? How can I make a Rails app do all of the same things that my Sinatra apps did? I have never been more excited to LEARN!

Well class is about to start... I am so hype to learn what all my peers discovered through last nights assignment (which btw was a very open ended learn something Railsy)! I am going to share testing with Rails using minitests (thank you Michael Hartl & Rails Tutorial)!

More Rails talk later!

### EDIT

I figured where else could I put this information other than with my first experience with Rails.  Let me begin by taking the stage with Sinatra.  Sinatra is a DSL (Digital Subscriber Line) web-framework, hidden inside a ruby gem `gem 'sinatra', '~> 1.4', '>= 1.4.5'` for creating web applications with little effort.  The complete development of this framework was made possible through many open source contributions and a lot of class.  

Working with Sinatra prior to Rails is how most Rubyists get their first experience creating APIs.  An API (Application Program Interface) is a set of routines, protocols, and tools for CRUD (Create Read Update Delete) functionality to build software applications.  It specifies how software components should interact and allows users to access databases for communication over the web.  Requests come from a user action and are sent to an API using the format method/verb/URL.

```
GET 'HTTP/URL'
Host: site.com
Foo: Bar
Key: Value
Cookie: Baz = Qux
```
A response is usually a string or JSON (JavaScript Object Notation) sent back to the user from the API.  This light-weight data exchange format is easy to read, write and transfer back and forth, which is why JSON formatting is preferred overall.  There are several common HTTP methods and verbs, however these are the most common:

POST = create

GET = read, sort, search, filter

PUT/PATCH = update

DELETE = destroy

Common HTTP status codes to use and look out for:

200 = OK

201 = created

301 = moved permanently

302 = found

304 = not modified

400 = bad request

401 = unauthorized

403 = forbidden

404 = not found

429 = too many requests

500 = internal server error

Now that we have dabbled a bit into everything else, here's a little more Rails talk for you!  Rails is a framework for web applications, software and APIs.  Some common mistakes by those not in the know: Ruby is NOT Rails and Rails is NOT Ruby, however, you cannot write a Rails app without Ruby (don't worry, we've all been there one time or another).  Rails follows a development pattern of MVC.  'M' stands for model, 'V' stands for views, and 'C' stands for controllers.  I intend to write a blog post entirely dedicated to MVC development in Rails, so more on that later.  For now, lets follow the same list pattern we've used thus far for this post, shall we?  Some frequently used Rails commands:

`rails new` generates a new Rails application.  If you wish to give a name to your application simply add it at the end of this command.

`rails db:` you can access the database of a Rails app with Application Record.  Through this command one can create, drop, migrate and perform all other relative db functions.  Beware `rails db:drop` unless you are working on your own private database and you can live with the consequences.

`rails generate` model, controller, view.  Rails can generate any file you need through this command, simply add your desire at the end.

`rails console` this command is similar to irb for Ruby.  You can run your code in a controlled environment without messing everything else up!

`rails test` If you did not run `rails new "#{insert_name_of_app_here}" -T` then you are running Minitest are your testing platform.  If you prefer to use RSpec, use the command above when generating your app, or if its too late for that, then you will need to remove all the test files related to Minitest and install the gem rspec-rails as follows:

```ruby
group :development, :test do
  gem 'rspec-rails', '~> 3.5'
end
```

Afterwards, you will need to run the commands `bundle install` to install the newly added gem and `rails generate rspec:install` to create a spec file and begin writing all your beautiful tests!

I think this will suffice for a first time Rails overview... for now.  BubbiesBlog is OUT!  MIC DROP!  Until next time, stay classy and code Ruby on Rails!
