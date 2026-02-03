# Late::ListInboxReviews200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** |  | [optional] |
| **data** | [**Array&lt;ListInboxReviews200ResponseDataInner&gt;**](ListInboxReviews200ResponseDataInner.md) |  | [optional] |
| **pagination** | [**ListInboxConversations200ResponsePagination**](ListInboxConversations200ResponsePagination.md) |  | [optional] |
| **meta** | [**ListInboxConversations200ResponseMeta**](ListInboxConversations200ResponseMeta.md) |  | [optional] |
| **summary** | [**ListInboxReviews200ResponseSummary**](ListInboxReviews200ResponseSummary.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::ListInboxReviews200Response.new(
  status: null,
  data: null,
  pagination: null,
  meta: null,
  summary: null
)
```

