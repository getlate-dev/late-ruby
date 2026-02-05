# Late::ListGoogleBusinessMedia200ResponseMediaItemsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Resource name | [optional] |
| **media_format** | **String** |  | [optional] |
| **source_url** | **String** |  | [optional] |
| **google_url** | **String** | Google-hosted URL | [optional] |
| **thumbnail_url** | **String** |  | [optional] |
| **description** | **String** |  | [optional] |
| **create_time** | **Time** |  | [optional] |
| **location_association** | [**ListGoogleBusinessMedia200ResponseMediaItemsInnerLocationAssociation**](ListGoogleBusinessMedia200ResponseMediaItemsInnerLocationAssociation.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::ListGoogleBusinessMedia200ResponseMediaItemsInner.new(
  name: null,
  media_format: null,
  source_url: null,
  google_url: null,
  thumbnail_url: null,
  description: null,
  create_time: null,
  location_association: null
)
```

