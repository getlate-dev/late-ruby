# Late::WebhookPayloadMessageMessageAttachmentsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Attachment type (image, video, file, sticker, audio) | [optional] |
| **url** | **String** | Attachment URL (may expire for Meta platforms) | [optional] |
| **payload** | **Object** | Additional attachment metadata | [optional] |

## Example

```ruby
require 'late'

instance = Late::WebhookPayloadMessageMessageAttachmentsInner.new(
  type: null,
  url: null,
  payload: null
)
```

