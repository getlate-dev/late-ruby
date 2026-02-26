# Late::GetDailyMetrics200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **daily_data** | [**Array&lt;GetDailyMetrics200ResponseDailyDataInner&gt;**](GetDailyMetrics200ResponseDailyDataInner.md) |  | [optional] |
| **platform_breakdown** | [**Array&lt;GetDailyMetrics200ResponsePlatformBreakdownInner&gt;**](GetDailyMetrics200ResponsePlatformBreakdownInner.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetDailyMetrics200Response.new(
  daily_data: null,
  platform_breakdown: null
)
```

