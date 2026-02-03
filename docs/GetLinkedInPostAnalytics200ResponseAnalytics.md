# Late::GetLinkedInPostAnalytics200ResponseAnalytics

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **impressions** | **Integer** | Times the post was shown | [optional] |
| **reach** | **Integer** | Unique members who saw the post | [optional] |
| **likes** | **Integer** | Reactions on the post | [optional] |
| **comments** | **Integer** | Comments on the post | [optional] |
| **shares** | **Integer** | Reshares of the post | [optional] |
| **clicks** | **Integer** | Clicks on the post (organization accounts only) | [optional] |
| **views** | **Integer** | Video views (video posts only) | [optional] |
| **engagement_rate** | **Float** | Engagement rate as percentage | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetLinkedInPostAnalytics200ResponseAnalytics.new(
  impressions: null,
  reach: null,
  likes: null,
  comments: null,
  shares: null,
  clicks: null,
  views: null,
  engagement_rate: null
)
```

