# Late::UsageStats

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **plan_name** | **String** |  | [optional] |
| **billing_period** | **String** |  | [optional] |
| **signup_date** | **Time** |  | [optional] |
| **limits** | [**UsageStatsLimits**](UsageStatsLimits.md) |  | [optional] |
| **usage** | [**UsageStatsUsage**](UsageStatsUsage.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::UsageStats.new(
  plan_name: null,
  billing_period: null,
  signup_date: null,
  limits: null,
  usage: null
)
```

