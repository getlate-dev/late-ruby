# Late::SendInboxMessageRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** | Social account ID |  |
| **message** | **String** | Message text | [optional] |
| **quick_replies** | [**Array&lt;SendInboxMessageRequestQuickRepliesInner&gt;**](SendInboxMessageRequestQuickRepliesInner.md) | Quick reply buttons. Mutually exclusive with buttons. Max 13 items. | [optional] |
| **buttons** | [**Array&lt;SendInboxMessageRequestButtonsInner&gt;**](SendInboxMessageRequestButtonsInner.md) | Action buttons. Mutually exclusive with quickReplies. Max 3 items. | [optional] |
| **template** | [**SendInboxMessageRequestTemplate**](SendInboxMessageRequestTemplate.md) |  | [optional] |
| **reply_markup** | [**SendInboxMessageRequestReplyMarkup**](SendInboxMessageRequestReplyMarkup.md) |  | [optional] |
| **messaging_type** | **String** | Facebook messaging type. Required when using messageTag. | [optional] |
| **message_tag** | **String** | Facebook message tag for messaging outside 24h window. Requires messagingType MESSAGE_TAG. Instagram only supports HUMAN_AGENT. | [optional] |
| **reply_to** | **String** | Platform message ID to reply to (Telegram only). | [optional] |

## Example

```ruby
require 'late'

instance = Late::SendInboxMessageRequest.new(
  account_id: null,
  message: null,
  quick_replies: null,
  buttons: null,
  template: null,
  reply_markup: null,
  messaging_type: null,
  message_tag: null,
  reply_to: null
)
```

