# Check

[![travis][1]][2]

Redis backed service for monitoring metric data streams against
pre-defined thresholds.

## Installation

Add this line to your application's Gemfile:

    gem 'check'

And then run:

    $ bundle

Don't forget to leave the groups which you don't want/need out:

    $ bundle install --without check_api

Or install it yourself as:

    $ gem install check

## Usage

Check the examples directory. To run a specific example:

    $ ruby examples/metric_check.rb

NB: you will need to have all gems in `check_development` group installed.

## Benchmarks

Check the benchmarks directory. To run a specific benchmark:

    $ ruby benchmarks/metric_check.rb

NB: you will need to have all gems in `check_development` group installed.

## API

The gem comes with a self-contained API. It's powered by grape and
it includes a config.ru and unicorn.conf. Unicorn is **not** declared as
a dependency, feel free to choose whichever ruby web server you prefer
in the service implementing this gem.

All API dependencies have been declared in a separate group, you can
always `bundle install --without check_api`.

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Added some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

[1]: https://secure.travis-ci.org/gosquared/check.png
[2]: http://travis-ci.org/gosquared/check
