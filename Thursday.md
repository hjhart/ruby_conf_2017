# Day 2

# Just a minute

An enjoyable way to listen to a panel of speakers.

# Dispelling the dark magic: Inside a ruby debugger. Daniel Azuma.

TracePoint class is essential for building a debugger.a

Step in will execute the line of code that you're on and step into the method execution (if it has a stack to go down).
Step over will execute the line of code that you're on but not step into that method. Something I'm always missing slightly with binding.pry. The correct keyword in `pry-byebug` is `next`. Further documentation [here](https://github.com/deivid-rodriguez/pry-byebug).

When you drop into the default ruby irb debugger using TracePoint, it applies the context globally, not any particular thread. There is a C api that allows you do have thread specific context.

Threw the terms "Guilds" and "Code jails" in reference to immutability. 

There have been a few talks about functional languages, and how object states changing in the life cycle of a program being undesirable in some cases.

Stackdriver debugger is a debugger written by google. Might be worth looking at, not sure. He didn't really sell it.

# Tim Mertens - Intermittent failures and how to fix 'em.

Inside of a describe block in RSpec is not a namespace. You will be mutating global state if you define methods or CONSTANTS within a describe block.
Use `contain_exactly` or `match_array` when order of a result set does not matter
Prefer Timecop#travel to Timecop#freeze (why? didn't catch it. Check the talk notes)

# High value tests - noel rappin.

`workflow.run` intermediate workflow objects. they take params and the output is database changes.
he breaks down specs into System, Worfklow, and Unit tests.
The slowest specs represent the majority of the run time.
Unit tests will probably not save you time when you write the feature, but, there is value in long term costs... bug fixing, understanding code.
Rails 5 Test Prescriptions book. "NOLA RubyConf" should give you a 15% discount.

# Loading 1M lines of in 5 seconds.

Utiltizing autoloading is important. Rails does this automatically, but is important contextually because their api app is sinatra.
Referenced "bootsnap" gem from shopify


# GEM IDEA: Understand the amount of tests in each class, end-to-end, system, workflow and unit

We can submit this data to a centralized server and people can compare their products against other people's projects.
BOth give you an understanding of "how long these tests took to write" and "how much they take to run"

# GEM IDEA: rspec-activerecord-errors-warn

Sometimes when you switch development or CI environments (e.g. switching to docker) all of a sudden you have failures due to activerecord records being invalid, but we are not explicitly raising errors when we're creating these errors.
Create a gem that issues a warning when activerecord produces error messages on a created object (hook into factorygirl?)

# TODO: Rubocop linting
