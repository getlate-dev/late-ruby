# Late::ValidateApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**validate_media**](ValidateApi.md#validate_media) | **POST** /v1/tools/validate/media | Validate media URL |
| [**validate_post**](ValidateApi.md#validate_post) | **POST** /v1/tools/validate/post | Validate post content |
| [**validate_post_length**](ValidateApi.md#validate_post_length) | **POST** /v1/tools/validate/post-length | Validate post character count |
| [**validate_subreddit**](ValidateApi.md#validate_subreddit) | **GET** /v1/tools/validate/subreddit | Check subreddit existence |


## validate_media

> <ValidateMedia200Response> validate_media(validate_media_request)

Validate media URL

Check if a media URL is accessible and return metadata (content type, file size) plus per-platform size limit comparisons.  Performs a HEAD request (with GET fallback) to detect content type and size. Rejects private/localhost URLs for SSRF protection.  Platform limits are sourced from each platform's actual upload constraints. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ValidateApi.new
validate_media_request = Late::ValidateMediaRequest.new({url: 'https://example.com/image.jpg'}) # ValidateMediaRequest | 

begin
  # Validate media URL
  result = api_instance.validate_media(validate_media_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling ValidateApi->validate_media: #{e}"
end
```

#### Using the validate_media_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ValidateMedia200Response>, Integer, Hash)> validate_media_with_http_info(validate_media_request)

```ruby
begin
  # Validate media URL
  data, status_code, headers = api_instance.validate_media_with_http_info(validate_media_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ValidateMedia200Response>
rescue Late::ApiError => e
  puts "Error when calling ValidateApi->validate_media_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **validate_media_request** | [**ValidateMediaRequest**](ValidateMediaRequest.md) |  |  |

### Return type

[**ValidateMedia200Response**](ValidateMedia200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## validate_post

> <ValidatePost200Response> validate_post(validate_post_request)

Validate post content

Dry-run the full post validation pipeline without publishing. Catches issues like missing media for Instagram/TikTok/YouTube, hashtag limits, invalid thread formats, Facebook Reel requirements, and character limit violations.  Accepts the same body as `POST /v1/posts`. Does NOT validate accounts, process media, or track usage. This is content-only validation.  Returns errors for failures and warnings for near-limit content (>90% of character limit). 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ValidateApi.new
validate_post_request = Late::ValidatePostRequest.new({platforms: [{"platform": "youtube"}, {"platform": "twitter"}]}) # ValidatePostRequest | 

begin
  # Validate post content
  result = api_instance.validate_post(validate_post_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling ValidateApi->validate_post: #{e}"
end
```

#### Using the validate_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ValidatePost200Response>, Integer, Hash)> validate_post_with_http_info(validate_post_request)

```ruby
begin
  # Validate post content
  data, status_code, headers = api_instance.validate_post_with_http_info(validate_post_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ValidatePost200Response>
rescue Late::ApiError => e
  puts "Error when calling ValidateApi->validate_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **validate_post_request** | [**ValidatePostRequest**](ValidatePostRequest.md) |  |  |

### Return type

[**ValidatePost200Response**](ValidatePost200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## validate_post_length

> <ValidatePostLength200Response> validate_post_length(validate_post_length_request)

Validate post character count

Check weighted character count per platform and whether the text is within each platform's limit.  Twitter/X uses weighted counting (URLs = 23 chars via t.co, emojis = 2 chars). All other platforms use plain character length.  Returns counts and limits for all 15 supported platform variants. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ValidateApi.new
validate_post_length_request = Late::ValidatePostLengthRequest.new({text: 'Check out https://getlate.dev for scheduling posts!'}) # ValidatePostLengthRequest | 

begin
  # Validate post character count
  result = api_instance.validate_post_length(validate_post_length_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling ValidateApi->validate_post_length: #{e}"
end
```

#### Using the validate_post_length_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ValidatePostLength200Response>, Integer, Hash)> validate_post_length_with_http_info(validate_post_length_request)

```ruby
begin
  # Validate post character count
  data, status_code, headers = api_instance.validate_post_length_with_http_info(validate_post_length_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ValidatePostLength200Response>
rescue Late::ApiError => e
  puts "Error when calling ValidateApi->validate_post_length_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **validate_post_length_request** | [**ValidatePostLengthRequest**](ValidatePostLengthRequest.md) |  |  |

### Return type

[**ValidatePostLength200Response**](ValidatePostLength200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## validate_subreddit

> <ValidateSubreddit200Response> validate_subreddit(name)

Check subreddit existence

Check if a subreddit exists and return basic info (title, subscriber count, NSFW status, post types allowed).  Uses Reddit's public JSON API (no Reddit auth needed). Returns `exists: false` for private, banned, or nonexistent subreddits. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ValidateApi.new
name = 'programming' # String | Subreddit name (with or without \"r/\" prefix)

begin
  # Check subreddit existence
  result = api_instance.validate_subreddit(name)
  p result
rescue Late::ApiError => e
  puts "Error when calling ValidateApi->validate_subreddit: #{e}"
end
```

#### Using the validate_subreddit_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ValidateSubreddit200Response>, Integer, Hash)> validate_subreddit_with_http_info(name)

```ruby
begin
  # Check subreddit existence
  data, status_code, headers = api_instance.validate_subreddit_with_http_info(name)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ValidateSubreddit200Response>
rescue Late::ApiError => e
  puts "Error when calling ValidateApi->validate_subreddit_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Subreddit name (with or without \&quot;r/\&quot; prefix) |  |

### Return type

[**ValidateSubreddit200Response**](ValidateSubreddit200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

