# Late::SendInboxMessageRequestQuickRepliesInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **title** | **String** | Button label (max 20 chars) |  |
| **payload** | **String** | Payload sent back on tap |  |
| **image_url** | **String** | Optional icon URL (Meta only) | [optional] |

## Example

```ruby
require 'late'

instance = Late::SendInboxMessageRequestQuickRepliesInner.new(
  title: null,
  payload: null,
  image_url: null
)
```

