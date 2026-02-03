# Late::LikeInboxComment200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** |  | [optional] |
| **comment_id** | **String** |  | [optional] |
| **liked** | **Boolean** |  | [optional] |
| **like_uri** | **String** | (Bluesky only) URI to use for unliking | [optional] |
| **platform** | **String** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::LikeInboxComment200Response.new(
  status: null,
  comment_id: null,
  liked: null,
  like_uri: null,
  platform: null
)
```

