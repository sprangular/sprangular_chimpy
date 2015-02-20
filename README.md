Sprangular Chimpy
===========

Mailchimp integration for [sprangular](https://github.com/sprangular/sprangular)

Installation
------------

Add sprangular_chimpy & [spree_chimpy](https://github.com/DynamoMTL/spree_chimpy) to your Gemfile:

```ruby
gem 'spree_chimpy',      github: 'DynamoMTL/spree_chimpy'
gem 'sprangular_chimpy', github: 'sprangular/sprangular_chimpy'
```

Bundle your dependencies and run the spree_chimpy installation generator:

```shell
bundle
bundle exec rails g spree_chimpy:install
```

Add `Sprangular.Chimpy` module as a dependency to your host apps module:

```coffee
angular.module 'MyApp', ['Sprangular', 'Sprangular.Chimpy']
```

Include `chimpy/subscribe.html` somewhere in your layout (in footer is recommended):

```html
  <ng-include src="'chimpy/subscribe.html'"/>
```

Testing
-------

First bundle your dependencies, then run `rake`. `rake` will default to building the dummy app if it does not exist, then it will run specs. The dummy app can be regenerated by using `rake test_app`.

```shell
bundle
bundle exec rake
```

Copyright (c) 2015 Dynamo, released under the New BSD License
