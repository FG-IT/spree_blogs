# Spree Blogs (Shopify Style Blogs For Spree 4.2)

Helps Shopify users move to Spree, bringing their existing Blogs, Posts and URL paths with them.

This Spree Extension is designed for Spree 4.2 upwards and requires the acts-as-taggable-on gem to provide the same tagging support as you get in Shopify blogs.

## Installation

1. Add this extension to your Gemfile with this line:

    ```ruby
    gem 'acts-as-taggable-on', '~> 6.0'
    gem 'spree_blogs', github: 'matthewkennedy/spree_blogs'
    ```

2. Install the gem using Bundler

    ```ruby
    bundle install
    ```

3. Copy & run migrations

    ```ruby
    bundle exec rails acts_as_taggable_on_engine:install:migrations
    bundle exec rails g spree_blogs:install
    ```

4. Restart your server

  If your server was running, restart it so that it can find the assets properly.

## Testing

First bundle your dependencies, then run `rake`. `rake` will default to building the dummy app if it does not exist, then it will run specs. The dummy app can be regenerated by using `rake test_app`.

```shell
bundle
bundle exec rake
```

When testing your applications integration with this extension you may use it's factories.
Simply add this require statement to your spec_helper:

```ruby
require 'spree_blogs/factories'
```

## ToDo

- Add recent posts
- Add page caching
- Write tests

## Contributing

If you'd like to contribute, please take a look at the
[instructions](CONTRIBUTING.md) for installing dependencies and crafting a good
pull request.

Copyright (c) 2020 Matthew Kennedy, released under the New BSD License
