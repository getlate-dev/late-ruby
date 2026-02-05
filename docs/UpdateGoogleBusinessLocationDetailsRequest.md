# Late::UpdateGoogleBusinessLocationDetailsRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **update_mask** | **String** | Required. Comma-separated fields to update (e.g. &#39;regularHours&#39;, &#39;specialHours&#39;, &#39;profile.description&#39;) |  |
| **regular_hours** | [**UpdateGoogleBusinessLocationDetailsRequestRegularHours**](UpdateGoogleBusinessLocationDetailsRequestRegularHours.md) |  | [optional] |
| **special_hours** | [**GetGoogleBusinessLocationDetails200ResponseSpecialHours**](GetGoogleBusinessLocationDetails200ResponseSpecialHours.md) |  | [optional] |
| **profile** | [**UpdateGoogleBusinessLocationDetailsRequestProfile**](UpdateGoogleBusinessLocationDetailsRequestProfile.md) |  | [optional] |
| **website_uri** | **String** |  | [optional] |
| **phone_numbers** | [**GetGoogleBusinessLocationDetails200ResponsePhoneNumbers**](GetGoogleBusinessLocationDetails200ResponsePhoneNumbers.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::UpdateGoogleBusinessLocationDetailsRequest.new(
  update_mask: null,
  regular_hours: null,
  special_hours: null,
  profile: null,
  website_uri: null,
  phone_numbers: null
)
```

