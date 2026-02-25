# Late::TwitterPlatformData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **reply_settings** | **String** | Controls who can reply to the tweet. \&quot;following\&quot; allows only people you follow, \&quot;mentionedUsers\&quot; allows only mentioned users, \&quot;subscribers\&quot; allows only subscribers. Omit for default (everyone can reply). For threads, applies to the first tweet only. | [optional] |
| **thread_items** | [**Array&lt;TwitterPlatformDataThreadItemsInner&gt;**](TwitterPlatformDataThreadItemsInner.md) | Sequence of tweets in a thread. First item is the root tweet. | [optional] |

## Example

```ruby
require 'late'

instance = Late::TwitterPlatformData.new(
  reply_settings: null,
  thread_items: null
)
```

