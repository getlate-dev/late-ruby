# Late::GetInboxPostComments200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** |  | [optional] |
| **comments** | [**Array&lt;GetInboxPostComments200ResponseCommentsInner&gt;**](GetInboxPostComments200ResponseCommentsInner.md) |  | [optional] |
| **pagination** | [**GetInboxPostComments200ResponsePagination**](GetInboxPostComments200ResponsePagination.md) |  | [optional] |
| **meta** | [**GetInboxPostComments200ResponseMeta**](GetInboxPostComments200ResponseMeta.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetInboxPostComments200Response.new(
  status: null,
  comments: null,
  pagination: null,
  meta: null
)
```

