# Late::TwitterEngagementApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**bookmark_post**](TwitterEngagementApi.md#bookmark_post) | **POST** /v1/twitter/bookmark | Bookmark a tweet |
| [**follow_user**](TwitterEngagementApi.md#follow_user) | **POST** /v1/twitter/follow | Follow a user |
| [**remove_bookmark**](TwitterEngagementApi.md#remove_bookmark) | **DELETE** /v1/twitter/bookmark | Remove bookmark |
| [**retweet_post**](TwitterEngagementApi.md#retweet_post) | **POST** /v1/twitter/retweet | Retweet a post |
| [**undo_retweet**](TwitterEngagementApi.md#undo_retweet) | **DELETE** /v1/twitter/retweet | Undo retweet |
| [**unfollow_user**](TwitterEngagementApi.md#unfollow_user) | **DELETE** /v1/twitter/follow | Unfollow a user |


## bookmark_post

> <BookmarkPost200Response> bookmark_post(bookmark_post_request)

Bookmark a tweet

Bookmark a tweet by ID. Requires X API Basic tier ($200/mo) or higher. Requires the bookmark.write OAuth scope. Rate limit: 50 requests per 15-min window. 

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::TwitterEngagementApi.new
bookmark_post_request = Late::BookmarkPostRequest.new({account_id: 'account_id_example', tweet_id: 'tweet_id_example'}) # BookmarkPostRequest | 

begin
  # Bookmark a tweet
  result = api_instance.bookmark_post(bookmark_post_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling TwitterEngagementApi->bookmark_post: #{e}"
end
```

#### Using the bookmark_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BookmarkPost200Response>, Integer, Hash)> bookmark_post_with_http_info(bookmark_post_request)

```ruby
begin
  # Bookmark a tweet
  data, status_code, headers = api_instance.bookmark_post_with_http_info(bookmark_post_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BookmarkPost200Response>
rescue Late::ApiError => e
  puts "Error when calling TwitterEngagementApi->bookmark_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **bookmark_post_request** | [**BookmarkPostRequest**](BookmarkPostRequest.md) |  |  |

### Return type

[**BookmarkPost200Response**](BookmarkPost200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## follow_user

> <FollowUser200Response> follow_user(follow_user_request)

Follow a user

Follow a user on X/Twitter. Requires X API Basic tier ($200/mo) or higher. Requires the follows.write OAuth scope. For protected accounts, a follow request is sent instead (pending_follow will be true). 

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::TwitterEngagementApi.new
follow_user_request = Late::FollowUserRequest.new({account_id: 'account_id_example', target_user_id: 'target_user_id_example'}) # FollowUserRequest | 

begin
  # Follow a user
  result = api_instance.follow_user(follow_user_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling TwitterEngagementApi->follow_user: #{e}"
end
```

#### Using the follow_user_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FollowUser200Response>, Integer, Hash)> follow_user_with_http_info(follow_user_request)

```ruby
begin
  # Follow a user
  data, status_code, headers = api_instance.follow_user_with_http_info(follow_user_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FollowUser200Response>
rescue Late::ApiError => e
  puts "Error when calling TwitterEngagementApi->follow_user_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **follow_user_request** | [**FollowUserRequest**](FollowUserRequest.md) |  |  |

### Return type

[**FollowUser200Response**](FollowUser200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## remove_bookmark

> <RemoveBookmark200Response> remove_bookmark(account_id, tweet_id)

Remove bookmark

Remove a bookmark from a tweet. 

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::TwitterEngagementApi.new
account_id = 'account_id_example' # String | 
tweet_id = 'tweet_id_example' # String | The ID of the tweet to unbookmark

begin
  # Remove bookmark
  result = api_instance.remove_bookmark(account_id, tweet_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling TwitterEngagementApi->remove_bookmark: #{e}"
end
```

#### Using the remove_bookmark_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RemoveBookmark200Response>, Integer, Hash)> remove_bookmark_with_http_info(account_id, tweet_id)

```ruby
begin
  # Remove bookmark
  data, status_code, headers = api_instance.remove_bookmark_with_http_info(account_id, tweet_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RemoveBookmark200Response>
rescue Late::ApiError => e
  puts "Error when calling TwitterEngagementApi->remove_bookmark_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |
| **tweet_id** | **String** | The ID of the tweet to unbookmark |  |

### Return type

[**RemoveBookmark200Response**](RemoveBookmark200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## retweet_post

> <RetweetPost200Response> retweet_post(retweet_post_request)

Retweet a post

Retweet (repost) a tweet by ID. Requires X API Basic tier ($200/mo) or higher. Rate limit: 50 requests per 15-min window. Shares the 300/3hr creation limit with tweet creation. 

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::TwitterEngagementApi.new
retweet_post_request = Late::RetweetPostRequest.new({account_id: 'account_id_example', tweet_id: 'tweet_id_example'}) # RetweetPostRequest | 

begin
  # Retweet a post
  result = api_instance.retweet_post(retweet_post_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling TwitterEngagementApi->retweet_post: #{e}"
end
```

#### Using the retweet_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RetweetPost200Response>, Integer, Hash)> retweet_post_with_http_info(retweet_post_request)

```ruby
begin
  # Retweet a post
  data, status_code, headers = api_instance.retweet_post_with_http_info(retweet_post_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RetweetPost200Response>
rescue Late::ApiError => e
  puts "Error when calling TwitterEngagementApi->retweet_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **retweet_post_request** | [**RetweetPostRequest**](RetweetPostRequest.md) |  |  |

### Return type

[**RetweetPost200Response**](RetweetPost200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## undo_retweet

> <UndoRetweet200Response> undo_retweet(account_id, tweet_id)

Undo retweet

Undo a retweet (un-repost a tweet). 

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::TwitterEngagementApi.new
account_id = 'account_id_example' # String | 
tweet_id = 'tweet_id_example' # String | The ID of the original tweet to un-retweet

begin
  # Undo retweet
  result = api_instance.undo_retweet(account_id, tweet_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling TwitterEngagementApi->undo_retweet: #{e}"
end
```

#### Using the undo_retweet_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UndoRetweet200Response>, Integer, Hash)> undo_retweet_with_http_info(account_id, tweet_id)

```ruby
begin
  # Undo retweet
  data, status_code, headers = api_instance.undo_retweet_with_http_info(account_id, tweet_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UndoRetweet200Response>
rescue Late::ApiError => e
  puts "Error when calling TwitterEngagementApi->undo_retweet_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |
| **tweet_id** | **String** | The ID of the original tweet to un-retweet |  |

### Return type

[**UndoRetweet200Response**](UndoRetweet200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## unfollow_user

> <UnfollowUser200Response> unfollow_user(account_id, target_user_id)

Unfollow a user

Unfollow a user on X/Twitter. 

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::TwitterEngagementApi.new
account_id = 'account_id_example' # String | 
target_user_id = 'target_user_id_example' # String | The Twitter ID of the user to unfollow

begin
  # Unfollow a user
  result = api_instance.unfollow_user(account_id, target_user_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling TwitterEngagementApi->unfollow_user: #{e}"
end
```

#### Using the unfollow_user_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UnfollowUser200Response>, Integer, Hash)> unfollow_user_with_http_info(account_id, target_user_id)

```ruby
begin
  # Unfollow a user
  data, status_code, headers = api_instance.unfollow_user_with_http_info(account_id, target_user_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UnfollowUser200Response>
rescue Late::ApiError => e
  puts "Error when calling TwitterEngagementApi->unfollow_user_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |
| **target_user_id** | **String** | The Twitter ID of the user to unfollow |  |

### Return type

[**UnfollowUser200Response**](UnfollowUser200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

