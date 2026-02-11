# Late::WebhookPayloadMessage

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **event** | **String** |  | [optional] |
| **message** | [**WebhookPayloadMessageMessage**](WebhookPayloadMessageMessage.md) |  | [optional] |
| **conversation** | [**WebhookPayloadMessageConversation**](WebhookPayloadMessageConversation.md) |  | [optional] |
| **account** | [**WebhookPayloadMessageAccount**](WebhookPayloadMessageAccount.md) |  | [optional] |
| **metadata** | [**WebhookPayloadMessageMetadata**](WebhookPayloadMessageMetadata.md) |  | [optional] |
| **timestamp** | **Time** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::WebhookPayloadMessage.new(
  event: null,
  message: null,
  conversation: null,
  account: null,
  metadata: null,
  timestamp: null
)
```

