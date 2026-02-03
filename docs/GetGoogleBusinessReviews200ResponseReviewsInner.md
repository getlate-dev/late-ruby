# Late::GetGoogleBusinessReviews200ResponseReviewsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Review ID | [optional] |
| **name** | **String** | Full resource name | [optional] |
| **reviewer** | [**GetGoogleBusinessReviews200ResponseReviewsInnerReviewer**](GetGoogleBusinessReviews200ResponseReviewsInnerReviewer.md) |  | [optional] |
| **rating** | **Integer** | Numeric star rating | [optional] |
| **star_rating** | **String** | Google&#39;s string rating | [optional] |
| **comment** | **String** | Review text | [optional] |
| **create_time** | **Time** |  | [optional] |
| **update_time** | **Time** |  | [optional] |
| **review_reply** | [**GetGoogleBusinessReviews200ResponseReviewsInnerReviewReply**](GetGoogleBusinessReviews200ResponseReviewsInnerReviewReply.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetGoogleBusinessReviews200ResponseReviewsInner.new(
  id: null,
  name: null,
  reviewer: null,
  rating: null,
  star_rating: null,
  comment: null,
  create_time: null,
  update_time: null,
  review_reply: null
)
```

