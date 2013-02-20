Ember Rails Devise Demo
=======================

This app is working example of using Ember with Rails and Devise.  As Ember matures, I hope to expand it with other common Ember
paradigms.

**Disclaimer:** Ember.js is still very new and in flux, I am far from an expert, and documentation, though improving, is still not comprehensive.  While I intend to update and expand this demo with best practices as they become known to me, at present the code here should be viewed more as possible ways to get things done.  Welcome input on improvements.


Features
--------
* User Login and Registration using Devise
* Illustrates basic usages of Ember components like routes, controllers, views, templates, state managers.

Ember Version
-------------
This app runs currently runs on [Ember.js 1.0 RC1](http://emberjs.com/blog/2013/02/15/ember-1-0-rc/)

Getting Started
---------------

To run the app:

    (clone or fork the project)
    $ bundle install
    $ bundle exec rake db:create
    $ bundle exec rake db:migrate
    $ bundle exec rake db:seed    (will create a test user, or just register a new one from the app)
    $ rails server

Devise and JSON
---------------

When using Devise with AJAX you must add:

    respond_to :html, :json

to the appropriate Rails controller(s).  In this app, its been added to ApplicationController.  More [here](http://stackoverflow.com/questions/14319868/ember-js-with-devise-on-rails-application-406-not-acceptable-on-sign-up).

The Devise AJAX calls are in **javascripts/helpers/authentication_helper.js.coffee**

Tests
-----

There are a couple of capybara-webkit tests up.  The first tests a registration-logout-login cycle.  Was
going to separate these out, but the standalone login test doesn't work for some reason (even though works in development).
Appreciate if anyone can figure this out.

To Do
-----

Most immediately, **validations** and **tests** are sparse.  Plan to add features as time goes by.

Other Ember.js/Rails Resources
------------------------------

### Demos and Learning Resources

The official guides:

* http://emberjs.com/guides/

Peepcode

* [Ember.js Peepcode (Jan 2013)](https://peepcode.com/products/emberjs)

  Definitely worthwhile, though found it easier to watch it at 2X speed as recitation a tad slow
  
I found both of the following demos helpful (and new ones appearing all the time):

* [ember_data_examle](https://github.com/dgeb/ember_data_example)
* [ember_todo](https://github.com/Skalar/ember_todo)

### Add-ons

  Think HTML/Handlebars too verbose?  Alex Matchneer is developing a [Slim](http://slim-lang.com/)-like templating solution:

* [emblem.js](https://github.com/machty/emblem.js)



###License
Copyright 2013 Michael Madrid under the [MIT License](http://opensource.org/licenses/MIT)
