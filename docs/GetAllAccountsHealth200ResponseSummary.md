# Late::GetAllAccountsHealth200ResponseSummary

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **total** | **Integer** | Total number of accounts | [optional] |
| **healthy** | **Integer** | Number of healthy accounts | [optional] |
| **warning** | **Integer** | Number of accounts with warnings | [optional] |
| **error** | **Integer** | Number of accounts with errors | [optional] |
| **needs_reconnect** | **Integer** | Number of accounts needing reconnection | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetAllAccountsHealth200ResponseSummary.new(
  total: null,
  healthy: null,
  warning: null,
  error: null,
  needs_reconnect: null
)
```

