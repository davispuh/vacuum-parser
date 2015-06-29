# Vacuum::Parser

Parser for [Vacuum](https://github.com/hakanensari/vacuum)

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'vacuum-parser'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install vacuum-parser

## Usage

```ruby
require 'vacuum/parser'
Vacuum::Response.parser = Vacuum::Parser
response = request.item_search(...)
result = response.parse
if result.is_valid?
  puts result.items.to_a.first.item_attributes['Title']
else
  e = result.error
  raise "#{e['Code']}:#{e['Message']}"
end
```

## Contributing

1. Fork it ( https://github.com/davispuh/vacuum-parser/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
