# Late::GMBReviewsApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_google_business_reviews**](GMBReviewsApi.md#get_google_business_reviews) | **GET** /v1/accounts/{accountId}/gmb-reviews | Get reviews |


## get_google_business_reviews

> <GetGoogleBusinessReviews200Response> get_google_business_reviews(account_id, opts)

Get reviews

Fetches reviews for a connected Google Business Profile account. Returns all reviews including reviewer info, star rating, comment text, owner reply, and timestamps. Use pagination via nextPageToken for locations with many reviews. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::GMBReviewsApi.new
account_id = 'account_id_example' # String | The Late account ID (from /v1/accounts)
opts = {
  page_size: 56, # Integer | Number of reviews to fetch per page (max 50)
  page_token: 'page_token_example' # String | Pagination token from previous response
}

begin
  # Get reviews
  result = api_instance.get_google_business_reviews(account_id, opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling GMBReviewsApi->get_google_business_reviews: #{e}"
end
```

#### Using the get_google_business_reviews_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetGoogleBusinessReviews200Response>, Integer, Hash)> get_google_business_reviews_with_http_info(account_id, opts)

```ruby
begin
  # Get reviews
  data, status_code, headers = api_instance.get_google_business_reviews_with_http_info(account_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetGoogleBusinessReviews200Response>
rescue Late::ApiError => e
  puts "Error when calling GMBReviewsApi->get_google_business_reviews_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** | The Late account ID (from /v1/accounts) |  |
| **page_size** | **Integer** | Number of reviews to fetch per page (max 50) | [optional][default to 50] |
| **page_token** | **String** | Pagination token from previous response | [optional] |

### Return type

[**GetGoogleBusinessReviews200Response**](GetGoogleBusinessReviews200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

