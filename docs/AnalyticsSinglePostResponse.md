# Late::AnalyticsSinglePostResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_id** | **String** |  | [optional] |
| **status** | **String** |  | [optional] |
| **content** | **String** |  | [optional] |
| **scheduled_for** | **Time** |  | [optional] |
| **published_at** | **Time** |  | [optional] |
| **analytics** | [**PostAnalytics**](PostAnalytics.md) |  | [optional] |
| **platform_analytics** | [**Array&lt;PlatformAnalytics&gt;**](PlatformAnalytics.md) |  | [optional] |
| **platform** | **String** |  | [optional] |
| **platform_post_url** | **String** |  | [optional] |
| **is_external** | **Boolean** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::AnalyticsSinglePostResponse.new(
  post_id: null,
  status: null,
  content: null,
  scheduled_for: null,
  published_at: null,
  analytics: null,
  platform_analytics: null,
  platform: null,
  platform_post_url: null,
  is_external: null
)
```

