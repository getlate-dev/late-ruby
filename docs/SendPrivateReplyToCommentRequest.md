# Late::SendPrivateReplyToCommentRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** | The Instagram social account ID |  |
| **message** | **String** | The message text to send as a private DM |  |

## Example

```ruby
require 'late'

instance = Late::SendPrivateReplyToCommentRequest.new(
  account_id: null,
  message: null
)
```

