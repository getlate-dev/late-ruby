# Late::ListBroadcastRecipients200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **success** | **Boolean** |  | [optional] |
| **recipients** | [**Array&lt;ListBroadcastRecipients200ResponseRecipientsInner&gt;**](ListBroadcastRecipients200ResponseRecipientsInner.md) |  | [optional] |
| **pagination** | [**GetWhatsAppContacts200ResponsePagination**](GetWhatsAppContacts200ResponsePagination.md) |  | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::ListBroadcastRecipients200Response.new(
  success: null,
  recipients: null,
  pagination: null
)
```

