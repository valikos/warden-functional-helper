# Warden::Functional::Helper

This gem is a helper for functional testing in Rails with Rspec.

## Usage

```ruby
# Gemfile
group :test do
  gem 'warden-functional-helper', github: 'valikos/warden-functional-helper'
end

# spec_helper.rb
RSpec.configure do |c|
  c.include Warden::Functional::Helper, type: :controller

  def sign_in(user)
    warden.set_user(user)
  end
end
```
