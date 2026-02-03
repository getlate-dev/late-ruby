# Late::LinkedInAggregateAnalyticsDailyResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  | [optional] |
| **platform** | **String** |  | [optional] |
| **account_type** | **String** |  | [optional] |
| **username** | **String** |  | [optional] |
| **aggregation** | **String** |  | [optional] |
| **date_range** | [**LinkedInAggregateAnalyticsTotalResponseDateRange**](LinkedInAggregateAnalyticsTotalResponseDateRange.md) |  | [optional] |
| **analytics** | [**LinkedInAggregateAnalyticsDailyResponseAnalytics**](LinkedInAggregateAnalyticsDailyResponseAnalytics.md) |  | [optional] |
| **skipped_metrics** | **Array&lt;String&gt;** | Metrics that were skipped due to API limitations | [optional] |
| **note** | **String** |  | [optional] |
| **last_updated** | **Time** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::LinkedInAggregateAnalyticsDailyResponse.new(
  account_id: null,
  platform: linkedin,
  account_type: personal,
  username: null,
  aggregation: null,
  date_range: null,
  analytics: null,
  skipped_metrics: null,
  note: null,
  last_updated: null
)
```

