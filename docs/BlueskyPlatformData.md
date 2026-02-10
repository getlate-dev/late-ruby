# Late::BlueskyPlatformData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **thread_items** | [**Array&lt;TwitterPlatformDataThreadItemsInner&gt;**](TwitterPlatformDataThreadItemsInner.md) | Sequence of posts in a Bluesky thread (root then replies in order). | [optional] |

## Example

```ruby
require 'late'

instance = Late::BlueskyPlatformData.new(
  thread_items: null
)
```

