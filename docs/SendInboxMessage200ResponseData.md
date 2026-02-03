# Late::SendInboxMessage200ResponseData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message_id** | **String** | ID of the sent message (not returned for Reddit) | [optional] |
| **conversation_id** | **String** | Twitter conversation ID | [optional] |
| **sent_at** | **Time** | Bluesky sent timestamp | [optional] |
| **message** | **String** | Success message (Reddit only) | [optional] |

## Example

```ruby
require 'late'

instance = Late::SendInboxMessage200ResponseData.new(
  message_id: null,
  conversation_id: null,
  sent_at: null,
  message: null
)
```

