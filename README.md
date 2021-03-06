[![Circle CI](https://circleci.com/gh/constantcontact/fbaa-api.svg?style=svg)](https://circleci.com/gh/constantcontact/fbaa-api)

# FbaaApi

Welcome to your new gem! In this directory, you'll find the files you need to be able to package up your Ruby library into a gem. Put your Ruby code in the file `lib/fbaa_api`. To experiment with that code, run `bin/console` for an interactive prompt.

TODO: Delete this and the text above, and describe your gem

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'fbaa-api'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install fbaa-api

## Configuration

Configure the gem using the ```#configure``` method like so:

```ruby
  FbaaApi.configure do |c| 
    c.base_url    = 'https://example.com' # mandatory
    c.token       = 'yourtoken1234'       # mandatory, authentication token
    c.api_version = 'v1'                  # optional, defaults to v1
    c.logger      = Logger.new            * optional, defaults to STDOUT
  end
```

## Usage

```ruby
  FbaaApi.configure do |c| 
    # c.base_url = ... etc, etc
  end

  client = FbaaApi::Client.new

  client.create_ad(params)
  client.update_ad(id, params)
  client.get_ad(id, params)
  client.validate_image(params)
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/[USERNAME]/fbaa-api.

