# Late::RedditSearchApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_reddit_feed**](RedditSearchApi.md#get_reddit_feed) | **GET** /v1/reddit/feed | Get subreddit feed |
| [**search_reddit**](RedditSearchApi.md#search_reddit) | **GET** /v1/reddit/search | Search posts |


## get_reddit_feed

> <GetRedditFeed200Response> get_reddit_feed(account_id, opts)

Get subreddit feed

Fetch posts from a subreddit feed. Supports sorting, time filtering, and cursor-based pagination.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::RedditSearchApi.new
account_id = 'account_id_example' # String | 
opts = {
  subreddit: 'subreddit_example', # String | 
  sort: 'hot', # String | 
  limit: 56, # Integer | 
  after: 'after_example', # String | 
  t: 'hour' # String | 
}

begin
  # Get subreddit feed
  result = api_instance.get_reddit_feed(account_id, opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling RedditSearchApi->get_reddit_feed: #{e}"
end
```

#### Using the get_reddit_feed_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetRedditFeed200Response>, Integer, Hash)> get_reddit_feed_with_http_info(account_id, opts)

```ruby
begin
  # Get subreddit feed
  data, status_code, headers = api_instance.get_reddit_feed_with_http_info(account_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetRedditFeed200Response>
rescue Late::ApiError => e
  puts "Error when calling RedditSearchApi->get_reddit_feed_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |
| **subreddit** | **String** |  | [optional] |
| **sort** | **String** |  | [optional][default to &#39;hot&#39;] |
| **limit** | **Integer** |  | [optional][default to 25] |
| **after** | **String** |  | [optional] |
| **t** | **String** |  | [optional] |

### Return type

[**GetRedditFeed200Response**](GetRedditFeed200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## search_reddit

> <SearchReddit200Response> search_reddit(account_id, q, opts)

Search posts

Search Reddit posts using a connected account. Optionally scope to a specific subreddit.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::RedditSearchApi.new
account_id = 'account_id_example' # String | 
q = 'q_example' # String | 
opts = {
  subreddit: 'subreddit_example', # String | 
  restrict_sr: '0', # String | 
  sort: 'relevance', # String | 
  limit: 56, # Integer | 
  after: 'after_example' # String | 
}

begin
  # Search posts
  result = api_instance.search_reddit(account_id, q, opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling RedditSearchApi->search_reddit: #{e}"
end
```

#### Using the search_reddit_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SearchReddit200Response>, Integer, Hash)> search_reddit_with_http_info(account_id, q, opts)

```ruby
begin
  # Search posts
  data, status_code, headers = api_instance.search_reddit_with_http_info(account_id, q, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SearchReddit200Response>
rescue Late::ApiError => e
  puts "Error when calling RedditSearchApi->search_reddit_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |
| **q** | **String** |  |  |
| **subreddit** | **String** |  | [optional] |
| **restrict_sr** | **String** |  | [optional] |
| **sort** | **String** |  | [optional][default to &#39;new&#39;] |
| **limit** | **Integer** |  | [optional][default to 25] |
| **after** | **String** |  | [optional] |

### Return type

[**SearchReddit200Response**](SearchReddit200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

