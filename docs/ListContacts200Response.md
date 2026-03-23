# Late::ListContacts200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **success** | **Boolean** |  | [optional] |
| **contacts** | [**Array&lt;ListContacts200ResponseContactsInner&gt;**](ListContacts200ResponseContactsInner.md) |  | [optional] |
| **filters** | [**ListContacts200ResponseFilters**](ListContacts200ResponseFilters.md) |  | [optional] |
| **pagination** | [**GetWhatsAppContacts200ResponsePagination**](GetWhatsAppContacts200ResponsePagination.md) |  | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::ListContacts200Response.new(
  success: null,
  contacts: null,
  filters: null,
  pagination: null
)
```

