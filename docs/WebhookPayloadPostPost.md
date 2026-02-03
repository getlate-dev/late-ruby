# Late::WebhookPayloadPostPost

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  | [optional] |
| **content** | **String** |  | [optional] |
| **status** | **String** |  | [optional] |
| **scheduled_for** | **Time** |  | [optional] |
| **published_at** | **Time** |  | [optional] |
| **platforms** | [**Array&lt;WebhookPayloadPostPostPlatformsInner&gt;**](WebhookPayloadPostPostPlatformsInner.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::WebhookPayloadPostPost.new(
  id: null,
  content: null,
  status: null,
  scheduled_for: null,
  published_at: null,
  platforms: null
)
```

