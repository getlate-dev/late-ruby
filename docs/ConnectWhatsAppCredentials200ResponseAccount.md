# Late::ConnectWhatsAppCredentials200ResponseAccount

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  | [optional] |
| **platform** | **String** |  | [optional] |
| **username** | **String** | Display phone number | [optional] |
| **display_name** | **String** | Meta-verified business name | [optional] |
| **is_active** | **Boolean** |  | [optional] |
| **phone_number** | **String** |  | [optional] |
| **verified_name** | **String** |  | [optional] |
| **quality_rating** | **String** | GREEN, YELLOW, or RED | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::ConnectWhatsAppCredentials200ResponseAccount.new(
  account_id: null,
  platform: null,
  username: null,
  display_name: null,
  is_active: null,
  phone_number: null,
  verified_name: null,
  quality_rating: null
)
```

