# Late::ListGoogleBusinessMedia200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **success** | **Boolean** |  | [optional] |
| **account_id** | **String** |  | [optional] |
| **location_id** | **String** |  | [optional] |
| **media_items** | [**Array&lt;ListGoogleBusinessMedia200ResponseMediaItemsInner&gt;**](ListGoogleBusinessMedia200ResponseMediaItemsInner.md) |  | [optional] |
| **next_page_token** | **String** |  | [optional] |
| **total_media_items_count** | **Integer** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::ListGoogleBusinessMedia200Response.new(
  success: null,
  account_id: null,
  location_id: null,
  media_items: null,
  next_page_token: null,
  total_media_items_count: null
)
```

