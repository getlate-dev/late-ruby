# Late::GetBestTimeToPost200ResponseSlotsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **day_of_week** | **Integer** | 0&#x3D;Monday, 6&#x3D;Sunday | [optional] |
| **hour** | **Integer** | Hour in UTC (0-23) | [optional] |
| **avg_engagement** | **Float** | Average engagement (likes + comments + shares + saves) | [optional] |
| **post_count** | **Integer** | Number of posts in this slot | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetBestTimeToPost200ResponseSlotsInner.new(
  day_of_week: null,
  hour: null,
  avg_engagement: null,
  post_count: null
)
```

