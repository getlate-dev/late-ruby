# Late::GetDailyMetrics200ResponseDailyDataInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **date** | **String** |  | [optional] |
| **post_count** | **Integer** |  | [optional] |
| **platforms** | **Hash&lt;String, Integer&gt;** |  | [optional] |
| **metrics** | [**GetDailyMetrics200ResponseDailyDataInnerMetrics**](GetDailyMetrics200ResponseDailyDataInnerMetrics.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetDailyMetrics200ResponseDailyDataInner.new(
  date: 2025-12-01,
  post_count: 3,
  platforms: {&quot;instagram&quot;:2,&quot;twitter&quot;:1},
  metrics: null
)
```

