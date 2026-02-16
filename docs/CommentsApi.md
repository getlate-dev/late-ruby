# Late::CommentsApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**delete_inbox_comment**](CommentsApi.md#delete_inbox_comment) | **DELETE** /v1/inbox/comments/{postId} | Delete a comment |
| [**get_inbox_post_comments**](CommentsApi.md#get_inbox_post_comments) | **GET** /v1/inbox/comments/{postId} | Get comments for a post |
| [**hide_inbox_comment**](CommentsApi.md#hide_inbox_comment) | **POST** /v1/inbox/comments/{postId}/{commentId}/hide | Hide a comment |
| [**like_inbox_comment**](CommentsApi.md#like_inbox_comment) | **POST** /v1/inbox/comments/{postId}/{commentId}/like | Like a comment |
| [**list_inbox_comments**](CommentsApi.md#list_inbox_comments) | **GET** /v1/inbox/comments | List posts with comments across all accounts |
| [**reply_to_inbox_post**](CommentsApi.md#reply_to_inbox_post) | **POST** /v1/inbox/comments/{postId} | Reply to a post or comment |
| [**send_private_reply_to_comment**](CommentsApi.md#send_private_reply_to_comment) | **POST** /v1/inbox/comments/{postId}/{commentId}/private-reply | Send private reply to comment author |
| [**unhide_inbox_comment**](CommentsApi.md#unhide_inbox_comment) | **DELETE** /v1/inbox/comments/{postId}/{commentId}/hide | Unhide a comment |
| [**unlike_inbox_comment**](CommentsApi.md#unlike_inbox_comment) | **DELETE** /v1/inbox/comments/{postId}/{commentId}/like | Unlike a comment |


## delete_inbox_comment

> <DeleteInboxComment200Response> delete_inbox_comment(post_id, account_id, comment_id)

Delete a comment

Delete a comment on a post. Supported by Facebook, Instagram, Bluesky, Reddit, YouTube, LinkedIn, and TikTok. Requires accountId and commentId query parameters. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::CommentsApi.new
post_id = 'post_id_example' # String | The post identifier. Accepts a Late post ID or a platform-specific post ID.  **LinkedIn:** For third-party posts, pass the full activity URN (e.g., `urn:li:activity:7422459067685855232`) or the raw numeric activity ID from the URL. 
account_id = 'account_id_example' # String | 
comment_id = 'comment_id_example' # String | 

begin
  # Delete a comment
  result = api_instance.delete_inbox_comment(post_id, account_id, comment_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling CommentsApi->delete_inbox_comment: #{e}"
end
```

#### Using the delete_inbox_comment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeleteInboxComment200Response>, Integer, Hash)> delete_inbox_comment_with_http_info(post_id, account_id, comment_id)

```ruby
begin
  # Delete a comment
  data, status_code, headers = api_instance.delete_inbox_comment_with_http_info(post_id, account_id, comment_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeleteInboxComment200Response>
rescue Late::ApiError => e
  puts "Error when calling CommentsApi->delete_inbox_comment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_id** | **String** | The post identifier. Accepts a Late post ID or a platform-specific post ID.  **LinkedIn:** For third-party posts, pass the full activity URN (e.g., &#x60;urn:li:activity:7422459067685855232&#x60;) or the raw numeric activity ID from the URL.  |  |
| **account_id** | **String** |  |  |
| **comment_id** | **String** |  |  |

### Return type

[**DeleteInboxComment200Response**](DeleteInboxComment200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_inbox_post_comments

> <GetInboxPostComments200Response> get_inbox_post_comments(post_id, account_id, opts)

Get comments for a post

Fetch comments for a specific post. Requires accountId query parameter.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::CommentsApi.new
post_id = 'post_id_example' # String | The post identifier. Accepts a Late post ID (MongoDB ObjectId) which is automatically resolved to the platform-specific post ID, or a platform-specific post ID directly (e.g. tweet ID, Facebook Graph ID, YouTube video ID).  **LinkedIn:** For your own posts, the full URN stored in Late (e.g., `urn:li:share:7429218977714745345`) is used automatically. For third-party posts, pass either the full activity URN (e.g., `urn:li:activity:7422459067685855232`) or the raw numeric activity ID from the LinkedIn URL (automatically wrapped as `urn:li:activity:`). Note: LinkedIn post URLs use activity IDs (`linkedin.com/feed/update/urn:li:activity:XXXX`). 
account_id = 'account_id_example' # String | 
opts = {
  subreddit: 'subreddit_example', # String | (Reddit only) Subreddit name
  limit: 56, # Integer | Maximum number of comments to return
  cursor: 'cursor_example', # String | Pagination cursor
  comment_id: 'comment_id_example' # String | (Reddit only) Get replies to a specific comment
}

begin
  # Get comments for a post
  result = api_instance.get_inbox_post_comments(post_id, account_id, opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling CommentsApi->get_inbox_post_comments: #{e}"
end
```

#### Using the get_inbox_post_comments_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetInboxPostComments200Response>, Integer, Hash)> get_inbox_post_comments_with_http_info(post_id, account_id, opts)

```ruby
begin
  # Get comments for a post
  data, status_code, headers = api_instance.get_inbox_post_comments_with_http_info(post_id, account_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetInboxPostComments200Response>
rescue Late::ApiError => e
  puts "Error when calling CommentsApi->get_inbox_post_comments_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_id** | **String** | The post identifier. Accepts a Late post ID (MongoDB ObjectId) which is automatically resolved to the platform-specific post ID, or a platform-specific post ID directly (e.g. tweet ID, Facebook Graph ID, YouTube video ID).  **LinkedIn:** For your own posts, the full URN stored in Late (e.g., &#x60;urn:li:share:7429218977714745345&#x60;) is used automatically. For third-party posts, pass either the full activity URN (e.g., &#x60;urn:li:activity:7422459067685855232&#x60;) or the raw numeric activity ID from the LinkedIn URL (automatically wrapped as &#x60;urn:li:activity:&#x60;). Note: LinkedIn post URLs use activity IDs (&#x60;linkedin.com/feed/update/urn:li:activity:XXXX&#x60;).  |  |
| **account_id** | **String** |  |  |
| **subreddit** | **String** | (Reddit only) Subreddit name | [optional] |
| **limit** | **Integer** | Maximum number of comments to return | [optional][default to 25] |
| **cursor** | **String** | Pagination cursor | [optional] |
| **comment_id** | **String** | (Reddit only) Get replies to a specific comment | [optional] |

### Return type

[**GetInboxPostComments200Response**](GetInboxPostComments200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## hide_inbox_comment

> <HideInboxComment200Response> hide_inbox_comment(post_id, comment_id, hide_inbox_comment_request)

Hide a comment

Hide a comment on a post. Supported by Facebook, Instagram, and Threads. Hidden comments are only visible to the commenter and page admin. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::CommentsApi.new
post_id = 'post_id_example' # String | 
comment_id = 'comment_id_example' # String | 
hide_inbox_comment_request = Late::HideInboxCommentRequest.new({account_id: 'account_id_example'}) # HideInboxCommentRequest | 

begin
  # Hide a comment
  result = api_instance.hide_inbox_comment(post_id, comment_id, hide_inbox_comment_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling CommentsApi->hide_inbox_comment: #{e}"
end
```

#### Using the hide_inbox_comment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<HideInboxComment200Response>, Integer, Hash)> hide_inbox_comment_with_http_info(post_id, comment_id, hide_inbox_comment_request)

```ruby
begin
  # Hide a comment
  data, status_code, headers = api_instance.hide_inbox_comment_with_http_info(post_id, comment_id, hide_inbox_comment_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <HideInboxComment200Response>
rescue Late::ApiError => e
  puts "Error when calling CommentsApi->hide_inbox_comment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_id** | **String** |  |  |
| **comment_id** | **String** |  |  |
| **hide_inbox_comment_request** | [**HideInboxCommentRequest**](HideInboxCommentRequest.md) |  |  |

### Return type

[**HideInboxComment200Response**](HideInboxComment200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## like_inbox_comment

> <LikeInboxComment200Response> like_inbox_comment(post_id, comment_id, like_inbox_comment_request)

Like a comment

Like or upvote a comment on a post.  **Supported platforms:** Facebook, Twitter/X, Bluesky, Reddit  For Bluesky, the `cid` (content identifier) is required in the request body. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::CommentsApi.new
post_id = 'post_id_example' # String | 
comment_id = 'comment_id_example' # String | 
like_inbox_comment_request = Late::LikeInboxCommentRequest.new({account_id: 'account_id_example'}) # LikeInboxCommentRequest | 

begin
  # Like a comment
  result = api_instance.like_inbox_comment(post_id, comment_id, like_inbox_comment_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling CommentsApi->like_inbox_comment: #{e}"
end
```

#### Using the like_inbox_comment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<LikeInboxComment200Response>, Integer, Hash)> like_inbox_comment_with_http_info(post_id, comment_id, like_inbox_comment_request)

```ruby
begin
  # Like a comment
  data, status_code, headers = api_instance.like_inbox_comment_with_http_info(post_id, comment_id, like_inbox_comment_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <LikeInboxComment200Response>
rescue Late::ApiError => e
  puts "Error when calling CommentsApi->like_inbox_comment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_id** | **String** |  |  |
| **comment_id** | **String** |  |  |
| **like_inbox_comment_request** | [**LikeInboxCommentRequest**](LikeInboxCommentRequest.md) |  |  |

### Return type

[**LikeInboxComment200Response**](LikeInboxComment200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## list_inbox_comments

> <ListInboxComments200Response> list_inbox_comments(opts)

List posts with comments across all accounts

Fetch posts with their comment counts from all connected accounts. Aggregates data from multiple accounts in a single API call.  **Supported platforms:** Facebook, Instagram, Twitter/X, Bluesky, Threads, YouTube, LinkedIn, Reddit, TikTok (write-only) 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::CommentsApi.new
opts = {
  profile_id: 'profile_id_example', # String | Filter by profile ID
  platform: 'facebook', # String | Filter by platform
  min_comments: 56, # Integer | Minimum comment count
  since: Time.parse('2013-10-20T19:20:30+01:00'), # Time | Posts created after this date
  sort_by: 'date', # String | Sort field
  sort_order: 'asc', # String | Sort order
  limit: 56, # Integer | 
  cursor: 'cursor_example', # String | 
  account_id: 'account_id_example' # String | Filter by specific social account ID
}

begin
  # List posts with comments across all accounts
  result = api_instance.list_inbox_comments(opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling CommentsApi->list_inbox_comments: #{e}"
end
```

#### Using the list_inbox_comments_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListInboxComments200Response>, Integer, Hash)> list_inbox_comments_with_http_info(opts)

```ruby
begin
  # List posts with comments across all accounts
  data, status_code, headers = api_instance.list_inbox_comments_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListInboxComments200Response>
rescue Late::ApiError => e
  puts "Error when calling CommentsApi->list_inbox_comments_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** | Filter by profile ID | [optional] |
| **platform** | **String** | Filter by platform | [optional] |
| **min_comments** | **Integer** | Minimum comment count | [optional] |
| **since** | **Time** | Posts created after this date | [optional] |
| **sort_by** | **String** | Sort field | [optional][default to &#39;date&#39;] |
| **sort_order** | **String** | Sort order | [optional][default to &#39;desc&#39;] |
| **limit** | **Integer** |  | [optional][default to 50] |
| **cursor** | **String** |  | [optional] |
| **account_id** | **String** | Filter by specific social account ID | [optional] |

### Return type

[**ListInboxComments200Response**](ListInboxComments200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## reply_to_inbox_post

> <ReplyToInboxPost200Response> reply_to_inbox_post(post_id, reply_to_inbox_post_request)

Reply to a post or comment

Post a reply to a post or specific comment. Requires accountId in request body.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::CommentsApi.new
post_id = 'post_id_example' # String | The post identifier. Accepts a Late post ID or a platform-specific post ID.  **LinkedIn:** For third-party posts, pass the full activity URN (e.g., `urn:li:activity:7422459067685855232`) or the raw numeric activity ID from the URL. 
reply_to_inbox_post_request = Late::ReplyToInboxPostRequest.new({account_id: 'account_id_example', message: 'message_example'}) # ReplyToInboxPostRequest | 

begin
  # Reply to a post or comment
  result = api_instance.reply_to_inbox_post(post_id, reply_to_inbox_post_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling CommentsApi->reply_to_inbox_post: #{e}"
end
```

#### Using the reply_to_inbox_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ReplyToInboxPost200Response>, Integer, Hash)> reply_to_inbox_post_with_http_info(post_id, reply_to_inbox_post_request)

```ruby
begin
  # Reply to a post or comment
  data, status_code, headers = api_instance.reply_to_inbox_post_with_http_info(post_id, reply_to_inbox_post_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ReplyToInboxPost200Response>
rescue Late::ApiError => e
  puts "Error when calling CommentsApi->reply_to_inbox_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_id** | **String** | The post identifier. Accepts a Late post ID or a platform-specific post ID.  **LinkedIn:** For third-party posts, pass the full activity URN (e.g., &#x60;urn:li:activity:7422459067685855232&#x60;) or the raw numeric activity ID from the URL.  |  |
| **reply_to_inbox_post_request** | [**ReplyToInboxPostRequest**](ReplyToInboxPostRequest.md) |  |  |

### Return type

[**ReplyToInboxPost200Response**](ReplyToInboxPost200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## send_private_reply_to_comment

> <SendPrivateReplyToComment200Response> send_private_reply_to_comment(post_id, comment_id, send_private_reply_to_comment_request)

Send private reply to comment author

Send a private direct message to the author of a comment on your post. This is useful for handling customer inquiries or sensitive matters privately.  **Supported platforms:** Instagram, Facebook  **Limitations:** - Only ONE private reply per comment (platform API restriction) - Must be sent within 7 days of the comment being posted - Only works for comments on posts owned by the connected account - Text only (no media attachments) - Instagram: message goes to the user's Inbox (if they follow you) or Message Requests (if they don't). Requires `instagram_business_manage_messages` permission. - Facebook: message opens a Messenger conversation with the commenter. Requires `pages_messaging` permission.  **Note:** Both permissions are already included in Late's OAuth flow. This does not create a conversation thread until the user replies back. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::CommentsApi.new
post_id = 'post_id_example' # String | The media/post ID (Instagram media ID or Facebook post ID)
comment_id = 'comment_id_example' # String | The comment ID to send a private reply to
send_private_reply_to_comment_request = Late::SendPrivateReplyToCommentRequest.new({account_id: 'account_id_example', message: 'message_example'}) # SendPrivateReplyToCommentRequest | 

begin
  # Send private reply to comment author
  result = api_instance.send_private_reply_to_comment(post_id, comment_id, send_private_reply_to_comment_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling CommentsApi->send_private_reply_to_comment: #{e}"
end
```

#### Using the send_private_reply_to_comment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SendPrivateReplyToComment200Response>, Integer, Hash)> send_private_reply_to_comment_with_http_info(post_id, comment_id, send_private_reply_to_comment_request)

```ruby
begin
  # Send private reply to comment author
  data, status_code, headers = api_instance.send_private_reply_to_comment_with_http_info(post_id, comment_id, send_private_reply_to_comment_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SendPrivateReplyToComment200Response>
rescue Late::ApiError => e
  puts "Error when calling CommentsApi->send_private_reply_to_comment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_id** | **String** | The media/post ID (Instagram media ID or Facebook post ID) |  |
| **comment_id** | **String** | The comment ID to send a private reply to |  |
| **send_private_reply_to_comment_request** | [**SendPrivateReplyToCommentRequest**](SendPrivateReplyToCommentRequest.md) |  |  |

### Return type

[**SendPrivateReplyToComment200Response**](SendPrivateReplyToComment200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## unhide_inbox_comment

> <HideInboxComment200Response> unhide_inbox_comment(post_id, comment_id, account_id)

Unhide a comment

Unhide a previously hidden comment. Supported by Facebook, Instagram, and Threads. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::CommentsApi.new
post_id = 'post_id_example' # String | 
comment_id = 'comment_id_example' # String | 
account_id = 'account_id_example' # String | 

begin
  # Unhide a comment
  result = api_instance.unhide_inbox_comment(post_id, comment_id, account_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling CommentsApi->unhide_inbox_comment: #{e}"
end
```

#### Using the unhide_inbox_comment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<HideInboxComment200Response>, Integer, Hash)> unhide_inbox_comment_with_http_info(post_id, comment_id, account_id)

```ruby
begin
  # Unhide a comment
  data, status_code, headers = api_instance.unhide_inbox_comment_with_http_info(post_id, comment_id, account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <HideInboxComment200Response>
rescue Late::ApiError => e
  puts "Error when calling CommentsApi->unhide_inbox_comment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_id** | **String** |  |  |
| **comment_id** | **String** |  |  |
| **account_id** | **String** |  |  |

### Return type

[**HideInboxComment200Response**](HideInboxComment200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## unlike_inbox_comment

> <UnlikeInboxComment200Response> unlike_inbox_comment(post_id, comment_id, account_id, opts)

Unlike a comment

Remove a like from a comment.  **Supported platforms:** Facebook, Twitter/X, Bluesky, Reddit  For Bluesky, the `likeUri` query parameter is required. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::CommentsApi.new
post_id = 'post_id_example' # String | 
comment_id = 'comment_id_example' # String | 
account_id = 'account_id_example' # String | 
opts = {
  like_uri: 'like_uri_example' # String | (Bluesky only) The like URI returned when liking
}

begin
  # Unlike a comment
  result = api_instance.unlike_inbox_comment(post_id, comment_id, account_id, opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling CommentsApi->unlike_inbox_comment: #{e}"
end
```

#### Using the unlike_inbox_comment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UnlikeInboxComment200Response>, Integer, Hash)> unlike_inbox_comment_with_http_info(post_id, comment_id, account_id, opts)

```ruby
begin
  # Unlike a comment
  data, status_code, headers = api_instance.unlike_inbox_comment_with_http_info(post_id, comment_id, account_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UnlikeInboxComment200Response>
rescue Late::ApiError => e
  puts "Error when calling CommentsApi->unlike_inbox_comment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_id** | **String** |  |  |
| **comment_id** | **String** |  |  |
| **account_id** | **String** |  |  |
| **like_uri** | **String** | (Bluesky only) The like URI returned when liking | [optional] |

### Return type

[**UnlikeInboxComment200Response**](UnlikeInboxComment200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

