# Late::EditInboxMessageRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** | Social account ID |  |
| **text** | **String** | New message text | [optional] |
| **reply_markup** | [**EditInboxMessageRequestReplyMarkup**](EditInboxMessageRequestReplyMarkup.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::EditInboxMessageRequest.new(
  account_id: null,
  text: null,
  reply_markup: null
)
```

