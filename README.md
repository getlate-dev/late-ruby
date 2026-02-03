# Late Ruby SDK

Official Ruby client library for the [Late API](https://docs.getlate.dev) - Schedule and manage social media posts across multiple platforms.

## Installation

```bash
gem install late
```

Or add to your Gemfile:

```ruby
gem 'late'
```

## Quick Start

```ruby
require 'late'

Late.configure do |config|
  config.api_key['Authorization'] = 'Bearer YOUR_API_KEY'
end

api = Late::AccountsApi.new

# List accounts
accounts = api.list_accounts
puts accounts

# Create a post
posts_api = Late::PostsApi.new
post = posts_api.create_post({
  content: 'Hello from Ruby!',
  platforms: [{ platform: 'twitter', account_id: 'acc_123' }],
  publish_now: true
})
```

## Documentation

- [API Reference](https://docs.getlate.dev/api-reference)
- [Getting Started Guide](https://docs.getlate.dev/quickstart)

## License

MIT
