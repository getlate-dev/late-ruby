# Late::PostAnalytics

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **impressions** | **Integer** |  | [optional] |
| **reach** | **Integer** |  | [optional] |
| **likes** | **Integer** |  | [optional] |
| **comments** | **Integer** |  | [optional] |
| **shares** | **Integer** |  | [optional] |
| **clicks** | **Integer** |  | [optional] |
| **views** | **Integer** |  | [optional] |
| **engagement_rate** | **Float** |  | [optional] |
| **last_updated** | **Time** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::PostAnalytics.new(
  impressions: 0,
  reach: 0,
  likes: 0,
  comments: 0,
  shares: 0,
  clicks: 0,
  views: 0,
  engagement_rate: 0,
  last_updated: null
)
```

