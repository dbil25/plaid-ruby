# Plaid

Ruby bindings for the Plaid API

Warning: If you have been using any version < 1 please switch to the correct branch. 

## Installation

Add this line to your application's Gemfile:

```ruby
   gem 'plaid'
```

And install

    $ bundle

Or install it system wide as:

    $ gem install plaid

## Usage

Please read the great documentation at http://plaid.com/docs/ for more information.

Configure the gem with your customer id, secret key, and the environment path you would like to use.

```ruby
Plaid.config do |p|
    p.customer_id = ['test_id']
    p.secret = ['test_secret']
    p.environment_location = ['https://tartan.plaid.com/']
   end
```

Authenticate a user to your desired level of api access (auth / connect).

```ruby
    user = Plaid.auth('auth','plaid_test','plaid_good','wells')
```

## Learn More

Learn about the full functionality of the library on our [Wiki](https://github.com/plaid/plaid-ruby/wiki)

## Contribute

We highly encourage helping out with the gem. Either adding more tests, building new helper classes, fixing bugs, or anything to increase overall quality.

The rules for contributing are simple:

No outside runtime libraries are allowed unless approved by the maintainer.

Follow the workflow set up below. Bug fixes should be labeled as a hot-fix, features labeled as features

Semantic versioning is strictly adhered to.

If you build a new feature you must release an update to the readme with information about the feature before it is accepted and committed.

New rubygems versions will be based on test coverage and passing tests, or time span for smaller combined bug fixes.

Contribution rules:

*Fork it ( https://github.com/plaid/plaid-ruby/fork ) 2a) Create your feature branch (git checkout -b feature/my-new-feature) 2b) Create your new hot-fix branch (git checkout -b hot-fix/my-new-hotfix)
*Commit your changes
*Push to the branch (git push origin feature/my-new-feature)
*Create a new Pull Request
*Wait for review and merge or notes to get merge accepted