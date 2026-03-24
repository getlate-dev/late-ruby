# Late::ThreadsPlatformData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **topic_tag** | **String** | Topic tag for post categorization and discoverability on Threads. Must be 1-50 characters, cannot contain periods (.) or ampersands (&amp;). Overrides auto-extraction from content hashtags when provided. | [optional] |
| **thread_items** | [**Array&lt;TwitterPlatformDataThreadItemsInner&gt;**](TwitterPlatformDataThreadItemsInner.md) | Sequence of posts in a Threads thread (root then replies in order). | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::ThreadsPlatformData.new(
  topic_tag: null,
  thread_items: null
)
```

