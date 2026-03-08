# Late::GetPostTimeline200ResponseTimelineInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **date** | **Date** | Date in YYYY-MM-DD format | [optional] |
| **platform** | **String** | Platform name (e.g. instagram, tiktok) | [optional] |
| **platform_post_id** | **String** | Platform-specific post ID | [optional] |
| **impressions** | **Integer** | Total impressions on this date | [optional] |
| **reach** | **Integer** | Total reach on this date | [optional] |
| **likes** | **Integer** | Total likes on this date | [optional] |
| **comments** | **Integer** | Total comments on this date | [optional] |
| **shares** | **Integer** | Total shares on this date | [optional] |
| **saves** | **Integer** | Total saves on this date | [optional] |
| **clicks** | **Integer** | Total clicks on this date | [optional] |
| **views** | **Integer** | Total views on this date | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::GetPostTimeline200ResponseTimelineInner.new(
  date: null,
  platform: null,
  platform_post_id: null,
  impressions: null,
  reach: null,
  likes: null,
  comments: null,
  shares: null,
  saves: null,
  clicks: null,
  views: null
)
```

