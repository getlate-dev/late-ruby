# Late::GetPostTimeline200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_id** | **String** | The postId that was requested | [optional] |
| **timeline** | [**Array&lt;GetPostTimeline200ResponseTimelineInner&gt;**](GetPostTimeline200ResponseTimelineInner.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetPostTimeline200Response.new(
  post_id: null,
  timeline: null
)
```

