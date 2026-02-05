# Late::ListGoogleBusinessPlaceActions200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **success** | **Boolean** |  | [optional] |
| **account_id** | **String** |  | [optional] |
| **location_id** | **String** |  | [optional] |
| **place_action_links** | [**Array&lt;ListGoogleBusinessPlaceActions200ResponsePlaceActionLinksInner&gt;**](ListGoogleBusinessPlaceActions200ResponsePlaceActionLinksInner.md) |  | [optional] |
| **next_page_token** | **String** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::ListGoogleBusinessPlaceActions200Response.new(
  success: null,
  account_id: null,
  location_id: null,
  place_action_links: null,
  next_page_token: null
)
```

