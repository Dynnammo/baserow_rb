# BaserowRb
[![License](https://img.shields.io/badge/License-AGPL%20v3-blue.svg)](http://www.gnu.org/licenses/agpl-3.0)   


Welcome to your new gem! In this directory, you'll find the files you need to be able to package up your Ruby library into a gem. Put your Ruby code in the file `lib/baserow_rb`. To experiment with that code, run `bin/console` for an interactive prompt.

## Installation

TODO: Replace `baserow_rb` with your gem name right after releasing it to RubyGems.org. Please do not do it earlier due to security reasons. Alternatively, replace this section with instructions to install your gem from git if you don't plan to release to RubyGems.org.

Install the gem and add to the application's Gemfile by executing:

    $ bundle add baserow_rb

If bundler is not being used to manage dependencies, install the gem by executing:

    $ gem install baserow_rb

## Usage

TODO: Write usage instructions here

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and the created tag, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/[USERNAME]/baserow_rb.

## Specs
Aim of this gem is to provide an **easy and reliable way to use Baserow in a Ruby application**

As instance, if you have a database with tables `Articles`, `Customers` and `Sells`, it should provide the following Ruby classes with attributes corresponding to their columns
```ruby
TOKEN = "myprivatetoken"

bsr = Baserow.new(TOKEN) # generate a wrapper that can be used elsewhere to give access to all data 

a = Articles.all # return serialized articles
a = Articles.get(row_id: 1) # return article that have row_id equal to 1
puts a.name # Dynamic creation of accessors methods 
a.description = "My new description" # Dynamic creation of setters methods
```