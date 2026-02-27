# Late::ValidatePostRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **content** | **String** | Post text content | [optional] |
| **platforms** | [**Array&lt;ValidatePostRequestPlatformsInner&gt;**](ValidatePostRequestPlatformsInner.md) | Target platforms (same format as POST /v1/posts) |  |
| **media_items** | [**Array&lt;ValidatePostRequestMediaItemsInner&gt;**](ValidatePostRequestMediaItemsInner.md) | Root media items shared across platforms | [optional] |

## Example

```ruby
require 'late'

instance = Late::ValidatePostRequest.new(
  content: Check out this video!,
  platforms: [{&quot;platform&quot;:&quot;youtube&quot;},{&quot;platform&quot;:&quot;twitter&quot;}],
  media_items: null
)
```

