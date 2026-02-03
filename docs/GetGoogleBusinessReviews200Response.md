# Late::GetGoogleBusinessReviews200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **success** | **Boolean** |  | [optional] |
| **account_id** | **String** |  | [optional] |
| **location_id** | **String** |  | [optional] |
| **reviews** | [**Array&lt;GetGoogleBusinessReviews200ResponseReviewsInner&gt;**](GetGoogleBusinessReviews200ResponseReviewsInner.md) |  | [optional] |
| **average_rating** | **Float** | Overall average rating | [optional] |
| **total_review_count** | **Integer** | Total number of reviews | [optional] |
| **next_page_token** | **String** | Token for next page | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetGoogleBusinessReviews200Response.new(
  success: null,
  account_id: null,
  location_id: null,
  reviews: null,
  average_rating: null,
  total_review_count: null,
  next_page_token: null
)
```

