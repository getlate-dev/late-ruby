# Late::UpdatePostRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **content** | **String** |  | [optional] |
| **scheduled_for** | **Time** |  | [optional] |
| **tiktok_settings** | [**TikTokPlatformData**](TikTokPlatformData.md) | Root-level TikTok settings applied to all TikTok platforms. Merged into each platform&#39;s platformSpecificData, with platform-specific settings taking precedence. | [optional] |

## Example

```ruby
require 'late'

instance = Late::UpdatePostRequest.new(
  content: null,
  scheduled_for: null,
  tiktok_settings: null
)
```

