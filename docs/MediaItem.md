# Late::MediaItem

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  | [optional] |
| **url** | **String** |  | [optional] |
| **filename** | **String** |  | [optional] |
| **size** | **Integer** | Optional file size in bytes | [optional] |
| **mime_type** | **String** | Optional MIME type (e.g. image/jpeg, video/mp4) | [optional] |
| **thumbnail** | **String** | Optional thumbnail image URL for videos | [optional] |
| **instagram_thumbnail** | **String** | Optional custom cover image URL for Instagram Reels | [optional] |
| **tiktok_processed** | **Boolean** | Internal flag indicating the image was resized for TikTok | [optional] |

## Example

```ruby
require 'late'

instance = Late::MediaItem.new(
  type: null,
  url: null,
  filename: null,
  size: null,
  mime_type: null,
  thumbnail: null,
  instagram_thumbnail: null,
  tiktok_processed: null
)
```

