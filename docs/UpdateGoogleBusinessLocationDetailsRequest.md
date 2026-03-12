# Late::UpdateGoogleBusinessLocationDetailsRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **update_mask** | **String** | Required. Comma-separated fields to update (e.g. &#39;regularHours&#39;, &#39;specialHours&#39;, &#39;profile.description&#39;, &#39;categories&#39;, &#39;serviceItems&#39;). Any valid Google Business Information API updateMask field is supported. |  |
| **regular_hours** | [**UpdateGoogleBusinessLocationDetailsRequestRegularHours**](UpdateGoogleBusinessLocationDetailsRequestRegularHours.md) |  | [optional] |
| **special_hours** | [**GetGoogleBusinessLocationDetails200ResponseSpecialHours**](GetGoogleBusinessLocationDetails200ResponseSpecialHours.md) |  | [optional] |
| **profile** | [**UpdateGoogleBusinessLocationDetailsRequestProfile**](UpdateGoogleBusinessLocationDetailsRequestProfile.md) |  | [optional] |
| **website_uri** | **String** |  | [optional] |
| **phone_numbers** | [**GetGoogleBusinessLocationDetails200ResponsePhoneNumbers**](GetGoogleBusinessLocationDetails200ResponsePhoneNumbers.md) |  | [optional] |
| **categories** | [**UpdateGoogleBusinessLocationDetailsRequestCategories**](UpdateGoogleBusinessLocationDetailsRequestCategories.md) |  | [optional] |
| **service_items** | [**Array&lt;UpdateGoogleBusinessLocationDetailsRequestServiceItemsInner&gt;**](UpdateGoogleBusinessLocationDetailsRequestServiceItemsInner.md) | Services offered by the business. Use updateMask&#x3D;&#39;serviceItems&#39; to update. | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::UpdateGoogleBusinessLocationDetailsRequest.new(
  update_mask: null,
  regular_hours: null,
  special_hours: null,
  profile: null,
  website_uri: null,
  phone_numbers: null,
  categories: null,
  service_items: null
)
```

