# Late::PinterestPlatformData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **title** | **String** | Pin title. Defaults to first line of content or \&quot;Pin\&quot;. Must be ≤ 100 characters. | [optional] |
| **board_id** | **String** | Target Pinterest board ID. If omitted, the first available board is used. | [optional] |
| **link** | **String** | Destination link (pin URL) | [optional] |
| **cover_image_url** | **String** | Optional cover image for video pins | [optional] |
| **cover_image_key_frame_time** | **Integer** | Optional key frame time in seconds for derived video cover | [optional] |

## Example

```ruby
require 'late'

instance = Late::PinterestPlatformData.new(
  title: null,
  board_id: null,
  link: null,
  cover_image_url: null,
  cover_image_key_frame_time: null
)
```

