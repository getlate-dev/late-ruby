# Late::AnalyticsListResponsePostsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **_id** | **String** |  | [optional] |
| **late_post_id** | **String** | Original Late post ID if scheduled via Late | [optional] |
| **content** | **String** |  | [optional] |
| **scheduled_for** | **Time** |  | [optional] |
| **published_at** | **Time** |  | [optional] |
| **status** | **String** |  | [optional] |
| **analytics** | [**PostAnalytics**](PostAnalytics.md) |  | [optional] |
| **platforms** | [**Array&lt;PlatformAnalytics&gt;**](PlatformAnalytics.md) |  | [optional] |
| **platform** | **String** |  | [optional] |
| **platform_post_url** | **String** |  | [optional] |
| **is_external** | **Boolean** |  | [optional] |
| **profile_id** | **String** |  | [optional] |
| **thumbnail_url** | **String** |  | [optional] |
| **media_type** | **String** |  | [optional] |
| **media_items** | [**Array&lt;AnalyticsSinglePostResponseMediaItemsInner&gt;**](AnalyticsSinglePostResponseMediaItemsInner.md) | All media items for this post. Carousel posts contain one entry per slide. | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::AnalyticsListResponsePostsInner.new(
  _id: null,
  late_post_id: null,
  content: null,
  scheduled_for: null,
  published_at: null,
  status: null,
  analytics: null,
  platforms: null,
  platform: null,
  platform_post_url: null,
  is_external: null,
  profile_id: null,
  thumbnail_url: null,
  media_type: null,
  media_items: null
)
```

