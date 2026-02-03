# Late::InstagramPlatformDataTrialParams

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **graduation_strategy** | **String** | The graduation strategy specifies when a trial reel becomes a regular reel: - MANUAL: The trial reel can only be manually graduated from the native Instagram app. - SS_PERFORMANCE: The trial reel will be automatically graduated if it performs well with non-followers.  | [optional] |

## Example

```ruby
require 'late'

instance = Late::InstagramPlatformDataTrialParams.new(
  graduation_strategy: null
)
```

