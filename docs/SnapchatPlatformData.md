# Late::SnapchatPlatformData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **content_type** | **String** | Content type: story (ephemeral 24h, default), saved_story (permanent on Public Profile), spotlight (video feed) | [optional][default to &#39;story&#39;] |

## Example

```ruby
require 'late'

instance = Late::SnapchatPlatformData.new(
  content_type: null
)
```

