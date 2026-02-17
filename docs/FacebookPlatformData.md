# Late::FacebookPlatformData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **content_type** | **String** | Set to &#39;story&#39; to publish as a Facebook Page Story (24-hour ephemeral content). Requires media. | [optional] |
| **first_comment** | **String** | Optional first comment to post immediately after publishing (feed posts only, not stories) | [optional] |
| **page_id** | **String** | Target Facebook Page ID for multi-page posting. If omitted, uses the default page. Use GET /v1/accounts/{id}/facebook-page to list pages. | [optional] |

## Example

```ruby
require 'late'

instance = Late::FacebookPlatformData.new(
  content_type: null,
  first_comment: null,
  page_id: null
)
```

