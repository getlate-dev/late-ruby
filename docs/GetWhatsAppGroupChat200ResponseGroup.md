# Late::GetWhatsAppGroupChat200ResponseGroup

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  | [optional] |
| **subject** | **String** |  | [optional] |
| **description** | **String** |  | [optional] |
| **join_approval_mode** | **String** |  | [optional] |
| **participants** | [**Array&lt;GetWhatsAppGroupChat200ResponseGroupParticipantsInner&gt;**](GetWhatsAppGroupChat200ResponseGroupParticipantsInner.md) |  | [optional] |
| **participant_count** | **Integer** |  | [optional] |
| **created_at** | **Integer** | UNIX timestamp | [optional] |
| **is_suspended** | **Boolean** |  | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::GetWhatsAppGroupChat200ResponseGroup.new(
  id: null,
  subject: null,
  description: null,
  join_approval_mode: null,
  participants: null,
  participant_count: null,
  created_at: null,
  is_suspended: null
)
```

