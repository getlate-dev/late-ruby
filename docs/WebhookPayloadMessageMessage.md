# Late::WebhookPayloadMessageMessage

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Internal message ID | [optional] |
| **conversation_id** | **String** | Internal conversation ID | [optional] |
| **platform** | **String** |  | [optional] |
| **platform_message_id** | **String** | Platform&#39;s message ID | [optional] |
| **direction** | **String** |  | [optional] |
| **text** | **String** | Message text content | [optional] |
| **attachments** | [**Array&lt;WebhookPayloadMessageMessageAttachmentsInner&gt;**](WebhookPayloadMessageMessageAttachmentsInner.md) |  | [optional] |
| **sender** | [**WebhookPayloadMessageMessageSender**](WebhookPayloadMessageMessageSender.md) |  | [optional] |
| **sent_at** | **Time** |  | [optional] |
| **is_read** | **Boolean** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::WebhookPayloadMessageMessage.new(
  id: null,
  conversation_id: null,
  platform: null,
  platform_message_id: null,
  direction: null,
  text: null,
  attachments: null,
  sender: null,
  sent_at: null,
  is_read: null
)
```

