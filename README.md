# Alma

A client for Web Services provided by the Ex Libris's Alma Library System.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'alma', :git => https://github.com/tulibraries/alma.git
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install alma

## Usage

### Configuration

You'll need to configure the Alma gem to ensure you query the appropriate data. To do so in a rails app, create `config/initializers/alma.rb` with :

```ruby
Alma.configure do |config|
  # You have to set te apikey 
  config.apikey     = 'EXAMPLE_EL_DEV_NETWORK_APPLICATION_KEY'
  # Alma gem defaults to querying Ex Libris's North American  Api servers. You can override that here.
  config.region   = "https://api-eu.hosted.exlibrisgroup.com
end
```

Now you can access those configuration attributes with `Alma.configuration.apikey`

### Making Requests

#### Get a list of Users
 ```ruby
 users = Alma::User.find
 
 user.total count
 > 402
 
 user.first.id 
 > NoamV
 
 ```
## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/[USERNAME]/alma. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.


## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).
