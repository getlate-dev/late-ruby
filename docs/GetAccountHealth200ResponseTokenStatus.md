# Late::GetAccountHealth200ResponseTokenStatus

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **valid** | **Boolean** | Whether the token is valid | [optional] |
| **expires_at** | **Time** |  | [optional] |
| **expires_in** | **String** | Human-readable time until expiry | [optional] |
| **needs_refresh** | **Boolean** | Whether token expires within 24 hours | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetAccountHealth200ResponseTokenStatus.new(
  valid: null,
  expires_at: null,
  expires_in: null,
  needs_refresh: null
)
```

