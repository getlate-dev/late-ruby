# Late::CreateGoogleBusinessMediaRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **source_url** | **String** | Publicly accessible image URL |  |
| **media_format** | **String** |  | [optional][default to &#39;PHOTO&#39;] |
| **description** | **String** | Photo description | [optional] |
| **category** | **String** | Where the photo appears on the listing | [optional] |

## Example

```ruby
require 'late'

instance = Late::CreateGoogleBusinessMediaRequest.new(
  source_url: null,
  media_format: null,
  description: null,
  category: null
)
```

