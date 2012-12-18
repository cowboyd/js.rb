# js.rb - Embed JavasScript into Ruby

js.rb harnesses the power of JavaScript inside your Ruby application

## Synopsis

evaluate some simple JavaScript

    cxt = JS::Context.new
    cxt.eval('7 * 6') #=> 42

embed values into the scope of your context

    cxt['foo'] = "bar"
    cxt.eval('foo') # => "bar"

embed Ruby code into your scope and call it from JavaScript

    cxt["say"] = lambda {|this, word, times| word * times}
    cxt.eval("say('Hello', 3)") #=> HelloHelloHello

## Installation

Add this line to your application's Gemfile:

    gem 'js'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install js

