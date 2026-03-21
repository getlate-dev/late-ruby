# Late::GetTikTokCreatorInfo200ResponsePostingLimits

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **max_video_duration_sec** | **Integer** | Maximum video duration in seconds | [optional] |
| **interaction_settings** | **Object** | Available interaction toggles (comment, duet, stitch) and their defaults | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::GetTikTokCreatorInfo200ResponsePostingLimits.new(
  max_video_duration_sec: null,
  interaction_settings: null
)
```

