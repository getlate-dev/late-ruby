# Late::GetLinkedInAggregateAnalytics403Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **error** | **String** |  | [optional] |
| **code** | **String** |  | [optional] |
| **required_scope** | **String** |  | [optional] |
| **action** | **String** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetLinkedInAggregateAnalytics403Response.new(
  error: null,
  code: missing_scope,
  required_scope: r_member_postAnalytics,
  action: reconnect
)
```

