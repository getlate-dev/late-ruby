# Late::UpdatePostMetadataRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **platform** | **String** | The platform to update metadata on |  |
| **video_id** | **String** | YouTube video ID (required for direct mode, ignored for post-based mode) | [optional] |
| **account_id** | **String** | Zernio social account ID (required for direct mode, ignored for post-based mode) | [optional] |
| **title** | **String** | New video title (max 100 characters for YouTube) | [optional] |
| **description** | **String** | New video description | [optional] |
| **tags** | **Array&lt;String&gt;** | Array of keyword tags (max 500 characters combined for YouTube) | [optional] |
| **category_id** | **String** | YouTube video category ID | [optional] |
| **privacy_status** | **String** | Video privacy setting | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::UpdatePostMetadataRequest.new(
  platform: null,
  video_id: null,
  account_id: null,
  title: null,
  description: null,
  tags: null,
  category_id: null,
  privacy_status: null
)
```

