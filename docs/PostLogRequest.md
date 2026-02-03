# Late::PostLogRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **content_preview** | **String** | First 200 chars of caption | [optional] |
| **media_count** | **Integer** |  | [optional] |
| **media_types** | **Array&lt;String&gt;** |  | [optional] |
| **media_urls** | **Array&lt;String&gt;** | URLs of media items sent to platform | [optional] |
| **scheduled_for** | **Time** |  | [optional] |
| **raw_body** | **String** | Full request body JSON (max 5000 chars) | [optional] |

## Example

```ruby
require 'late'

instance = Late::PostLogRequest.new(
  content_preview: null,
  media_count: null,
  media_types: null,
  media_urls: null,
  scheduled_for: null,
  raw_body: null
)
```

