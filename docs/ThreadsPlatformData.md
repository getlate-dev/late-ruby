# Late::ThreadsPlatformData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **thread_items** | [**Array&lt;TwitterPlatformDataThreadItemsInner&gt;**](TwitterPlatformDataThreadItemsInner.md) | Sequence of posts in a Threads thread (root then replies in order). | [optional] |

## Example

```ruby
require 'late'

instance = Late::ThreadsPlatformData.new(
  thread_items: null
)
```

