# Late::ListInboxReviews200ResponseDataInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  | [optional] |
| **platform** | **String** |  | [optional] |
| **account_id** | **String** |  | [optional] |
| **account_username** | **String** |  | [optional] |
| **reviewer** | [**ListInboxReviews200ResponseDataInnerReviewer**](ListInboxReviews200ResponseDataInnerReviewer.md) |  | [optional] |
| **rating** | **Integer** |  | [optional] |
| **text** | **String** |  | [optional] |
| **created** | **Time** |  | [optional] |
| **has_reply** | **Boolean** |  | [optional] |
| **reply** | [**ListInboxReviews200ResponseDataInnerReply**](ListInboxReviews200ResponseDataInnerReply.md) |  | [optional] |
| **review_url** | **String** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::ListInboxReviews200ResponseDataInner.new(
  id: null,
  platform: null,
  account_id: null,
  account_username: null,
  reviewer: null,
  rating: null,
  text: null,
  created: null,
  has_reply: null,
  reply: null,
  review_url: null
)
```

