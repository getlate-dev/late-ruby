# Late::PlatformAnalyticsAccountMetrics

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **followers** | **Integer** | Followers/fans count (e.g., Instagram, Facebook Pages, Twitter) | [optional] |
| **subscribers** | **Integer** | Subscribers count (e.g., YouTube) | [optional] |
| **last_updated** | **Time** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::PlatformAnalyticsAccountMetrics.new(
  followers: null,
  subscribers: null,
  last_updated: null
)
```

