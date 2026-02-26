# Late::GetPostingFrequency200ResponseFrequencyInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **platform** | **String** |  | [optional] |
| **posts_per_week** | **Integer** | Number of posts published that week | [optional] |
| **avg_engagement_rate** | **Float** | Average engagement rate as percentage (0-100) | [optional] |
| **avg_engagement** | **Float** | Average raw engagement (likes+comments+shares+saves) | [optional] |
| **weeks_count** | **Integer** | Number of calendar weeks observed at this frequency | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetPostingFrequency200ResponseFrequencyInner.new(
  platform: instagram,
  posts_per_week: null,
  avg_engagement_rate: null,
  avg_engagement: null,
  weeks_count: null
)
```

