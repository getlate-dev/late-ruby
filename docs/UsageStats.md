# Late::UsageStats

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **plan_name** | **String** |  | [optional] |
| **billing_period** | **String** |  | [optional] |
| **signup_date** | **Time** |  | [optional] |
| **billing_anchor_day** | **Integer** | Day of month (1-31) when the billing cycle resets | [optional] |
| **limits** | [**UsageStatsLimits**](UsageStatsLimits.md) |  | [optional] |
| **usage** | [**UsageStatsUsage**](UsageStatsUsage.md) |  | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::UsageStats.new(
  plan_name: null,
  billing_period: null,
  signup_date: null,
  billing_anchor_day: null,
  limits: null,
  usage: null
)
```

