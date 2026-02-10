# Late::ConnectionLogError

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **code** | **String** | Error code (e.g., oauth_denied, token_exchange_failed) | [optional] |
| **message** | **String** | Human-readable error message | [optional] |
| **raw_response** | **String** | Raw error response (truncated to 2000 chars) | [optional] |

## Example

```ruby
require 'late'

instance = Late::ConnectionLogError.new(
  code: null,
  message: null,
  raw_response: null
)
```

