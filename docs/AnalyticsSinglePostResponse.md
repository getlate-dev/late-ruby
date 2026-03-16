# Late::AnalyticsSinglePostResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_id** | **String** |  | [optional] |
| **late_post_id** | **String** | Original Late post ID if scheduled via Late | [optional] |
| **status** | **String** | Overall post status. \&quot;partial\&quot; when some platforms published and others failed. | [optional] |
| **content** | **String** |  | [optional] |
| **scheduled_for** | **Time** |  | [optional] |
| **published_at** | **Time** |  | [optional] |
| **analytics** | [**PostAnalytics**](PostAnalytics.md) |  | [optional] |
| **platform_analytics** | [**Array&lt;PlatformAnalytics&gt;**](PlatformAnalytics.md) |  | [optional] |
| **platform** | **String** |  | [optional] |
| **platform_post_url** | **String** |  | [optional] |
| **is_external** | **Boolean** |  | [optional] |
| **sync_status** | **String** | Overall sync state across all platforms | [optional] |
| **message** | **String** | Human-readable status message for pending, partial, or failed states | [optional] |
| **thumbnail_url** | **String** |  | [optional] |
| **media_type** | **String** |  | [optional] |
| **media_items** | [**Array&lt;AnalyticsSinglePostResponseMediaItemsInner&gt;**](AnalyticsSinglePostResponseMediaItemsInner.md) | All media items for this post. Carousel posts contain one entry per slide. | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::AnalyticsSinglePostResponse.new(
  post_id: null,
  late_post_id: null,
  status: null,
  content: null,
  scheduled_for: null,
  published_at: null,
  analytics: null,
  platform_analytics: null,
  platform: null,
  platform_post_url: null,
  is_external: null,
  sync_status: null,
  message: null,
  thumbnail_url: null,
  media_type: null,
  media_items: null
)
```

