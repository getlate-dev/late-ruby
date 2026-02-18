# Late::FacebookPlatformData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **content_type** | **String** | Set to &#39;story&#39; for Page Stories (24h ephemeral) or &#39;reel&#39; for Reels (short vertical video). Defaults to feed post if omitted. | [optional] |
| **title** | **String** | Reel title (only for contentType&#x3D;reel). Separate from the caption/content field. | [optional] |
| **first_comment** | **String** | Optional first comment to post immediately after publishing (feed posts only, not stories or reels) | [optional] |
| **page_id** | **String** | Target Facebook Page ID for multi-page posting. If omitted, uses the default page. Use GET /v1/accounts/{id}/facebook-page to list pages. | [optional] |

## Example

```ruby
require 'late'

instance = Late::FacebookPlatformData.new(
  content_type: null,
  title: null,
  first_comment: null,
  page_id: null
)
```

