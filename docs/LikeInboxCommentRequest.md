# Late::LikeInboxCommentRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** | The social account ID |  |
| **cid** | **String** | (Bluesky only) Content identifier for the comment | [optional] |

## Example

```ruby
require 'late'

instance = Late::LikeInboxCommentRequest.new(
  account_id: null,
  cid: null
)
```

