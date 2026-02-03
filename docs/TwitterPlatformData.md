# Late::TwitterPlatformData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **thread_items** | [**Array&lt;TwitterPlatformDataThreadItemsInner&gt;**](TwitterPlatformDataThreadItemsInner.md) | Sequence of tweets in a thread. First item is the root tweet. | [optional] |

## Example

```ruby
require 'late'

instance = Late::TwitterPlatformData.new(
  thread_items: null
)
```

