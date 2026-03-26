# Late::CreateWhatsAppGroupChatRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** | WhatsApp social account ID |  |
| **subject** | **String** | Group name (max 128 characters) |  |
| **description** | **String** | Group description (max 2048 characters) | [optional] |
| **join_approval_mode** | **String** | Whether users need approval to join via invite link | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::CreateWhatsAppGroupChatRequest.new(
  account_id: null,
  subject: null,
  description: null,
  join_approval_mode: null
)
```

