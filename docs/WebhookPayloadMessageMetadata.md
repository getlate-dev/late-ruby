# Late::WebhookPayloadMessageMetadata

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **quick_reply_payload** | **String** | Payload from a quick reply tap (Meta platforms) | [optional] |
| **postback_payload** | **String** | Payload from a postback button tap (Meta platforms) | [optional] |
| **postback_title** | **String** | Title of the tapped postback button (Meta platforms) | [optional] |
| **callback_data** | **String** | Callback data from an inline keyboard button tap (Telegram) | [optional] |

## Example

```ruby
require 'late'

instance = Late::WebhookPayloadMessageMetadata.new(
  quick_reply_payload: null,
  postback_payload: null,
  postback_title: null,
  callback_data: null
)
```

