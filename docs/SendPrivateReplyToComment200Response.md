# Late::SendPrivateReplyToComment200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** |  | [optional] |
| **message_id** | **String** | The ID of the sent message | [optional] |
| **comment_id** | **String** | The comment ID that was replied to | [optional] |
| **platform** | **String** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::SendPrivateReplyToComment200Response.new(
  status: success,
  message_id: null,
  comment_id: null,
  platform: instagram
)
```

