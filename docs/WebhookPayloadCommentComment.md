# Late::WebhookPayloadCommentComment

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Platform comment ID | [optional] |
| **post_id** | **String** | Internal post ID | [optional] |
| **platform_post_id** | **String** | Platform&#39;s post ID | [optional] |
| **platform** | **String** |  | [optional] |
| **text** | **String** | Comment text content | [optional] |
| **author** | [**WebhookPayloadCommentCommentAuthor**](WebhookPayloadCommentCommentAuthor.md) |  | [optional] |
| **created_at** | **Time** |  | [optional] |
| **is_reply** | **Boolean** | Whether this is a reply to another comment | [optional] |
| **parent_comment_id** | **String** | Parent comment ID if this is a reply | [optional] |

## Example

```ruby
require 'late'

instance = Late::WebhookPayloadCommentComment.new(
  id: null,
  post_id: null,
  platform_post_id: null,
  platform: null,
  text: null,
  author: null,
  created_at: null,
  is_reply: null,
  parent_comment_id: null
)
```

