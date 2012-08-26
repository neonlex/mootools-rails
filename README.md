# mootools-rails

MooTools! For Rails! So great.

This gem provides:

* MooTools 1.4.5
* MooTools More 1.4.0.1
* the latest MooTools UJS adapter
* modified version of Sam Ruby's assert_select_jquery function for MooTools, which is automatically included for use in tests

## Rails 3.1

For Rails 3.1 and greater, the files will be added to the asset pipeline and available for you to use. These two lines will be added to the file `app/assets/javascripts/application.js` by default:

    //= require mootools
    //= require mootools_ujs

If you wish to use MooTools More as well, you can add this line to `application.js`:

    //= require mootools-more

### Installation

When you generate a new Rails 3.1 app, pass the `-j mootools` option, like this:

    rails new myapp -j mootools

You're done!

## Rails 3.0

This gem adds a single generator to Rails 3, mootools:install. Running the generator will remove any Prototype JS files you may happen to have, fetch MooTools and the MooTools-ujs driver for Rails, and (optionally) fetch MooTools More.

The gem will also hook into the Rails configuration process, removing Prototype and adding MooTools to the javascript files included by the `javascript_include_tag(:defaults)` call. While the plugin downloads minified and un-minified versions of MooTools and MooTools More, only the minified versions are included in :default.

### Installation

In your Gemfile, add this line:

    gem "mootools-rails"

Then, run `bundle install`. To invoke the generator, run:

    rails generate mootools:install #--more to enable MooTools More

You're done!
