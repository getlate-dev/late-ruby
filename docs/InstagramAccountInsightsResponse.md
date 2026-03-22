# Late::InstagramAccountInsightsResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **success** | **Boolean** |  | [optional] |
| **account_id** | **String** | The Zernio SocialAccount ID | [optional] |
| **platform** | **String** |  | [optional] |
| **date_range** | [**InstagramAccountInsightsResponseDateRange**](InstagramAccountInsightsResponseDateRange.md) |  | [optional] |
| **metric_type** | **String** |  | [optional] |
| **breakdown** | **String** | Breakdown dimension used (only present when breakdown was requested) | [optional] |
| **metrics** | [**Hash&lt;String, InstagramAccountInsightsResponseMetricsValue&gt;**](InstagramAccountInsightsResponseMetricsValue.md) | Object keyed by metric name. For time_series: each metric has \&quot;total\&quot; (number) and \&quot;values\&quot; (array of {date, value}). For total_value: each metric has \&quot;total\&quot; (number) and optionally \&quot;breakdowns\&quot; (array of {dimension, value}).  | [optional] |
| **data_delay** | **String** |  | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::InstagramAccountInsightsResponse.new(
  success: true,
  account_id: null,
  platform: instagram,
  date_range: null,
  metric_type: null,
  breakdown: null,
  metrics: null,
  data_delay: Data may be delayed up to 48 hours
)
```

