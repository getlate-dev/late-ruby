# Late::GetGoogleBusinessLocationDetails200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **success** | **Boolean** |  | [optional] |
| **account_id** | **String** |  | [optional] |
| **location_id** | **String** |  | [optional] |
| **title** | **String** | Business name | [optional] |
| **regular_hours** | [**GetGoogleBusinessLocationDetails200ResponseRegularHours**](GetGoogleBusinessLocationDetails200ResponseRegularHours.md) |  | [optional] |
| **special_hours** | [**GetGoogleBusinessLocationDetails200ResponseSpecialHours**](GetGoogleBusinessLocationDetails200ResponseSpecialHours.md) |  | [optional] |
| **profile** | [**GetGoogleBusinessLocationDetails200ResponseProfile**](GetGoogleBusinessLocationDetails200ResponseProfile.md) |  | [optional] |
| **website_uri** | **String** |  | [optional] |
| **phone_numbers** | [**GetGoogleBusinessLocationDetails200ResponsePhoneNumbers**](GetGoogleBusinessLocationDetails200ResponsePhoneNumbers.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetGoogleBusinessLocationDetails200Response.new(
  success: null,
  account_id: null,
  location_id: null,
  title: null,
  regular_hours: null,
  special_hours: null,
  profile: null,
  website_uri: null,
  phone_numbers: null
)
```

