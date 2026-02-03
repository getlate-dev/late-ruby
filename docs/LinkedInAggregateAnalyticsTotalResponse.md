# Late::LinkedInAggregateAnalyticsTotalResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  | [optional] |
| **platform** | **String** |  | [optional] |
| **account_type** | **String** |  | [optional] |
| **username** | **String** |  | [optional] |
| **aggregation** | **String** |  | [optional] |
| **date_range** | [**LinkedInAggregateAnalyticsTotalResponseDateRange**](LinkedInAggregateAnalyticsTotalResponseDateRange.md) |  | [optional] |
| **analytics** | [**LinkedInAggregateAnalyticsTotalResponseAnalytics**](LinkedInAggregateAnalyticsTotalResponseAnalytics.md) |  | [optional] |
| **note** | **String** |  | [optional] |
| **last_updated** | **Time** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::LinkedInAggregateAnalyticsTotalResponse.new(
  account_id: null,
  platform: linkedin,
  account_type: personal,
  username: null,
  aggregation: null,
  date_range: null,
  analytics: null,
  note: null,
  last_updated: null
)
```

