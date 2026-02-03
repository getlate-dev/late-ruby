# Late::CreatePostRequestPlatformsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **platform** | **String** |  | [optional] |
| **account_id** | **String** |  | [optional] |
| **custom_content** | **String** |  | [optional] |
| **custom_media** | [**Array&lt;CreatePostRequestMediaItemsInner&gt;**](CreatePostRequestMediaItemsInner.md) |  | [optional] |
| **scheduled_for** | **Time** | Optional per-platform scheduled time override. When omitted, the top-level scheduledFor is used. | [optional] |
| **platform_specific_data** | [**CreatePostRequestPlatformsInnerPlatformSpecificData**](CreatePostRequestPlatformsInnerPlatformSpecificData.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::CreatePostRequestPlatformsInner.new(
  platform: twitter,
  account_id: null,
  custom_content: null,
  custom_media: null,
  scheduled_for: null,
  platform_specific_data: null
)
```

