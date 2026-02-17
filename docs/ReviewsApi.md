# Late::ReviewsApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**delete_inbox_review_reply**](ReviewsApi.md#delete_inbox_review_reply) | **DELETE** /v1/inbox/reviews/{reviewId}/reply | Delete review reply |
| [**list_inbox_reviews**](ReviewsApi.md#list_inbox_reviews) | **GET** /v1/inbox/reviews | List reviews |
| [**reply_to_inbox_review**](ReviewsApi.md#reply_to_inbox_review) | **POST** /v1/inbox/reviews/{reviewId}/reply | Reply to review |


## delete_inbox_review_reply

> <DeleteInboxReviewReply200Response> delete_inbox_review_reply(review_id, delete_inbox_review_reply_request)

Delete review reply

Delete a reply to a review (Google Business only). Requires accountId in request body.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ReviewsApi.new
review_id = 'review_id_example' # String | 
delete_inbox_review_reply_request = Late::DeleteInboxReviewReplyRequest.new({account_id: 'account_id_example'}) # DeleteInboxReviewReplyRequest | 

begin
  # Delete review reply
  result = api_instance.delete_inbox_review_reply(review_id, delete_inbox_review_reply_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling ReviewsApi->delete_inbox_review_reply: #{e}"
end
```

#### Using the delete_inbox_review_reply_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeleteInboxReviewReply200Response>, Integer, Hash)> delete_inbox_review_reply_with_http_info(review_id, delete_inbox_review_reply_request)

```ruby
begin
  # Delete review reply
  data, status_code, headers = api_instance.delete_inbox_review_reply_with_http_info(review_id, delete_inbox_review_reply_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeleteInboxReviewReply200Response>
rescue Late::ApiError => e
  puts "Error when calling ReviewsApi->delete_inbox_review_reply_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **review_id** | **String** |  |  |
| **delete_inbox_review_reply_request** | [**DeleteInboxReviewReplyRequest**](DeleteInboxReviewReplyRequest.md) |  |  |

### Return type

[**DeleteInboxReviewReply200Response**](DeleteInboxReviewReply200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## list_inbox_reviews

> <ListInboxReviews200Response> list_inbox_reviews(opts)

List reviews

Fetch reviews from all connected Facebook Pages and Google Business accounts. Aggregates data with filtering and sorting options.  **Supported platforms:** Facebook, Google Business 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ReviewsApi.new
opts = {
  profile_id: 'profile_id_example', # String | 
  platform: 'facebook', # String | 
  min_rating: 56, # Integer | 
  max_rating: 56, # Integer | 
  has_reply: true, # Boolean | Filter by reply status
  sort_by: 'date', # String | 
  sort_order: 'asc', # String | 
  limit: 56, # Integer | 
  cursor: 'cursor_example', # String | 
  account_id: 'account_id_example' # String | Filter by specific social account ID
}

begin
  # List reviews
  result = api_instance.list_inbox_reviews(opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling ReviewsApi->list_inbox_reviews: #{e}"
end
```

#### Using the list_inbox_reviews_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListInboxReviews200Response>, Integer, Hash)> list_inbox_reviews_with_http_info(opts)

```ruby
begin
  # List reviews
  data, status_code, headers = api_instance.list_inbox_reviews_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListInboxReviews200Response>
rescue Late::ApiError => e
  puts "Error when calling ReviewsApi->list_inbox_reviews_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** |  | [optional] |
| **platform** | **String** |  | [optional] |
| **min_rating** | **Integer** |  | [optional] |
| **max_rating** | **Integer** |  | [optional] |
| **has_reply** | **Boolean** | Filter by reply status | [optional] |
| **sort_by** | **String** |  | [optional][default to &#39;date&#39;] |
| **sort_order** | **String** |  | [optional][default to &#39;desc&#39;] |
| **limit** | **Integer** |  | [optional][default to 25] |
| **cursor** | **String** |  | [optional] |
| **account_id** | **String** | Filter by specific social account ID | [optional] |

### Return type

[**ListInboxReviews200Response**](ListInboxReviews200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## reply_to_inbox_review

> <ReplyToInboxReview200Response> reply_to_inbox_review(review_id, reply_to_inbox_review_request)

Reply to review

Post a reply to a review. Requires accountId in request body.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ReviewsApi.new
review_id = 'review_id_example' # String | Review ID (URL-encoded for Google Business)
reply_to_inbox_review_request = Late::ReplyToInboxReviewRequest.new({account_id: 'account_id_example', message: 'message_example'}) # ReplyToInboxReviewRequest | 

begin
  # Reply to review
  result = api_instance.reply_to_inbox_review(review_id, reply_to_inbox_review_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling ReviewsApi->reply_to_inbox_review: #{e}"
end
```

#### Using the reply_to_inbox_review_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ReplyToInboxReview200Response>, Integer, Hash)> reply_to_inbox_review_with_http_info(review_id, reply_to_inbox_review_request)

```ruby
begin
  # Reply to review
  data, status_code, headers = api_instance.reply_to_inbox_review_with_http_info(review_id, reply_to_inbox_review_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ReplyToInboxReview200Response>
rescue Late::ApiError => e
  puts "Error when calling ReviewsApi->reply_to_inbox_review_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **review_id** | **String** | Review ID (URL-encoded for Google Business) |  |
| **reply_to_inbox_review_request** | [**ReplyToInboxReviewRequest**](ReplyToInboxReviewRequest.md) |  |  |

### Return type

[**ReplyToInboxReview200Response**](ReplyToInboxReview200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

