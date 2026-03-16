# Late::AnalyticsOverview

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **total_posts** | **Integer** |  | [optional] |
| **published_posts** | **Integer** |  | [optional] |
| **scheduled_posts** | **Integer** |  | [optional] |
| **last_sync** | **Time** |  | [optional] |
| **data_staleness** | [**AnalyticsOverviewDataStaleness**](AnalyticsOverviewDataStaleness.md) |  | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::AnalyticsOverview.new(
  total_posts: null,
  published_posts: null,
  scheduled_posts: null,
  last_sync: null,
  data_staleness: null
)
```

