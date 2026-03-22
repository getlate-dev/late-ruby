# Late::InstagramAccountInsightsResponseMetricsValue

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **total** | **Float** | Sum or aggregate value for the metric | [optional] |
| **values** | [**Array&lt;InstagramAccountInsightsResponseMetricsValueValuesInner&gt;**](InstagramAccountInsightsResponseMetricsValueValuesInner.md) | Daily values (only for time_series) | [optional] |
| **breakdowns** | [**Array&lt;InstagramAccountInsightsResponseMetricsValueBreakdownsInner&gt;**](InstagramAccountInsightsResponseMetricsValueBreakdownsInner.md) | Breakdown values (only for total_value with breakdown) | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::InstagramAccountInsightsResponseMetricsValue.new(
  total: null,
  values: null,
  breakdowns: null
)
```

