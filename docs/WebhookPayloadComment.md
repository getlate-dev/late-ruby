# Late::WebhookPayloadComment

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **event** | **String** |  | [optional] |
| **comment** | [**WebhookPayloadCommentComment**](WebhookPayloadCommentComment.md) |  | [optional] |
| **post** | [**WebhookPayloadCommentPost**](WebhookPayloadCommentPost.md) |  | [optional] |
| **account** | [**WebhookPayloadCommentAccount**](WebhookPayloadCommentAccount.md) |  | [optional] |
| **timestamp** | **Time** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::WebhookPayloadComment.new(
  event: null,
  comment: null,
  post: null,
  account: null,
  timestamp: null
)
```

