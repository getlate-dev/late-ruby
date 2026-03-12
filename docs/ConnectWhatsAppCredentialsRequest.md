# Late::ConnectWhatsAppCredentialsRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** | Your Late profile ID |  |
| **access_token** | **String** | Permanent System User access token from Meta Business Suite |  |
| **waba_id** | **String** | WhatsApp Business Account ID from Meta |  |
| **phone_number_id** | **String** | Phone Number ID from Meta WhatsApp Manager |  |

## Example

```ruby
require 'late-sdk'

instance = Late::ConnectWhatsAppCredentialsRequest.new(
  profile_id: null,
  access_token: null,
  waba_id: null,
  phone_number_id: null
)
```

