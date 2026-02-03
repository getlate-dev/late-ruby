# Late::GetMediaPresignedUrlRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **filename** | **String** | Name of the file to upload |  |
| **content_type** | **String** | MIME type of the file |  |
| **size** | **Integer** | Optional file size in bytes for pre-validation (max 5GB) | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetMediaPresignedUrlRequest.new(
  filename: my-video.mp4,
  content_type: video/mp4,
  size: 15234567
)
```

