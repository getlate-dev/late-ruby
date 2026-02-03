# Late::SnapchatPlatformData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **content_type** | **String** | Type of Snapchat content to publish: - &#x60;story&#x60; - Ephemeral snap visible for 24 hours (default) - &#x60;saved_story&#x60; - Permanent story saved to Public Profile - &#x60;spotlight&#x60; - Video posted to Spotlight (Snapchat&#39;s TikTok-like feed)  | [optional][default to &#39;story&#39;] |

## Example

```ruby
require 'late'

instance = Late::SnapchatPlatformData.new(
  content_type: null
)
```

