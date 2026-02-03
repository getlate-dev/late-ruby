# Late::ToolsApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**check_instagram_hashtags**](ToolsApi.md#check_instagram_hashtags) | **POST** /v1/tools/instagram/hashtag-checker | Check Instagram hashtags for bans |
| [**download_bluesky_media**](ToolsApi.md#download_bluesky_media) | **GET** /v1/tools/bluesky/download | Download Bluesky video |
| [**download_facebook_video**](ToolsApi.md#download_facebook_video) | **GET** /v1/tools/facebook/download | Download Facebook video |
| [**download_instagram_media**](ToolsApi.md#download_instagram_media) | **GET** /v1/tools/instagram/download | Download Instagram reel or post |
| [**download_linked_in_video**](ToolsApi.md#download_linked_in_video) | **GET** /v1/tools/linkedin/download | Download LinkedIn video |
| [**download_tik_tok_video**](ToolsApi.md#download_tik_tok_video) | **GET** /v1/tools/tiktok/download | Download TikTok video |
| [**download_twitter_media**](ToolsApi.md#download_twitter_media) | **GET** /v1/tools/twitter/download | Download Twitter/X video |
| [**download_you_tube_video**](ToolsApi.md#download_you_tube_video) | **GET** /v1/tools/youtube/download | Download YouTube video or audio |
| [**get_you_tube_transcript**](ToolsApi.md#get_you_tube_transcript) | **GET** /v1/tools/youtube/transcript | Get YouTube video transcript |


## check_instagram_hashtags

> <CheckInstagramHashtags200Response> check_instagram_hashtags(check_instagram_hashtags_request)

Check Instagram hashtags for bans

Check if Instagram hashtags are banned, restricted, or safe to use.  **Rate Limits:** Build (50/day), Accelerate (500/day), Unlimited (unlimited) 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ToolsApi.new
check_instagram_hashtags_request = Late::CheckInstagramHashtagsRequest.new({hashtags: ["travel", "followforfollow", "fitness"]}) # CheckInstagramHashtagsRequest | 

begin
  # Check Instagram hashtags for bans
  result = api_instance.check_instagram_hashtags(check_instagram_hashtags_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling ToolsApi->check_instagram_hashtags: #{e}"
end
```

#### Using the check_instagram_hashtags_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CheckInstagramHashtags200Response>, Integer, Hash)> check_instagram_hashtags_with_http_info(check_instagram_hashtags_request)

```ruby
begin
  # Check Instagram hashtags for bans
  data, status_code, headers = api_instance.check_instagram_hashtags_with_http_info(check_instagram_hashtags_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CheckInstagramHashtags200Response>
rescue Late::ApiError => e
  puts "Error when calling ToolsApi->check_instagram_hashtags_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **check_instagram_hashtags_request** | [**CheckInstagramHashtagsRequest**](CheckInstagramHashtagsRequest.md) |  |  |

### Return type

[**CheckInstagramHashtags200Response**](CheckInstagramHashtags200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## download_bluesky_media

> <DownloadBlueskyMedia200Response> download_bluesky_media(url)

Download Bluesky video

Download videos from Bluesky posts.  **Rate Limits:** Build (50/day), Accelerate (500/day), Unlimited (unlimited) 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ToolsApi.new
url = 'https://bsky.app/profile/user.bsky.social/post/abc123' # String | Bluesky post URL

begin
  # Download Bluesky video
  result = api_instance.download_bluesky_media(url)
  p result
rescue Late::ApiError => e
  puts "Error when calling ToolsApi->download_bluesky_media: #{e}"
end
```

#### Using the download_bluesky_media_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DownloadBlueskyMedia200Response>, Integer, Hash)> download_bluesky_media_with_http_info(url)

```ruby
begin
  # Download Bluesky video
  data, status_code, headers = api_instance.download_bluesky_media_with_http_info(url)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DownloadBlueskyMedia200Response>
rescue Late::ApiError => e
  puts "Error when calling ToolsApi->download_bluesky_media_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | Bluesky post URL |  |

### Return type

[**DownloadBlueskyMedia200Response**](DownloadBlueskyMedia200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## download_facebook_video

> <DownloadFacebookVideo200Response> download_facebook_video(url)

Download Facebook video

Download videos and reels from Facebook.  **Rate Limits:** Build (50/day), Accelerate (500/day), Unlimited (unlimited) 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ToolsApi.new
url = 'url_example' # String | Facebook video or reel URL

begin
  # Download Facebook video
  result = api_instance.download_facebook_video(url)
  p result
rescue Late::ApiError => e
  puts "Error when calling ToolsApi->download_facebook_video: #{e}"
end
```

#### Using the download_facebook_video_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DownloadFacebookVideo200Response>, Integer, Hash)> download_facebook_video_with_http_info(url)

```ruby
begin
  # Download Facebook video
  data, status_code, headers = api_instance.download_facebook_video_with_http_info(url)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DownloadFacebookVideo200Response>
rescue Late::ApiError => e
  puts "Error when calling ToolsApi->download_facebook_video_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | Facebook video or reel URL |  |

### Return type

[**DownloadFacebookVideo200Response**](DownloadFacebookVideo200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## download_instagram_media

> <DownloadInstagramMedia200Response> download_instagram_media(url)

Download Instagram reel or post

Download Instagram reels, posts, or photos.  **Rate Limits:** Build (50/day), Accelerate (500/day), Unlimited (unlimited) 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ToolsApi.new
url = 'https://www.instagram.com/reel/ABC123/' # String | Instagram reel or post URL

begin
  # Download Instagram reel or post
  result = api_instance.download_instagram_media(url)
  p result
rescue Late::ApiError => e
  puts "Error when calling ToolsApi->download_instagram_media: #{e}"
end
```

#### Using the download_instagram_media_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DownloadInstagramMedia200Response>, Integer, Hash)> download_instagram_media_with_http_info(url)

```ruby
begin
  # Download Instagram reel or post
  data, status_code, headers = api_instance.download_instagram_media_with_http_info(url)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DownloadInstagramMedia200Response>
rescue Late::ApiError => e
  puts "Error when calling ToolsApi->download_instagram_media_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | Instagram reel or post URL |  |

### Return type

[**DownloadInstagramMedia200Response**](DownloadInstagramMedia200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## download_linked_in_video

> <DownloadInstagramMedia200Response> download_linked_in_video(url)

Download LinkedIn video

Download videos from LinkedIn posts.  **Rate Limits:** Build (50/day), Accelerate (500/day), Unlimited (unlimited) 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ToolsApi.new
url = 'url_example' # String | LinkedIn post URL

begin
  # Download LinkedIn video
  result = api_instance.download_linked_in_video(url)
  p result
rescue Late::ApiError => e
  puts "Error when calling ToolsApi->download_linked_in_video: #{e}"
end
```

#### Using the download_linked_in_video_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DownloadInstagramMedia200Response>, Integer, Hash)> download_linked_in_video_with_http_info(url)

```ruby
begin
  # Download LinkedIn video
  data, status_code, headers = api_instance.download_linked_in_video_with_http_info(url)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DownloadInstagramMedia200Response>
rescue Late::ApiError => e
  puts "Error when calling ToolsApi->download_linked_in_video_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | LinkedIn post URL |  |

### Return type

[**DownloadInstagramMedia200Response**](DownloadInstagramMedia200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## download_tik_tok_video

> <DownloadTikTokVideo200Response> download_tik_tok_video(url, opts)

Download TikTok video

Download TikTok videos with or without watermark.  **Rate Limits:** Build (50/day), Accelerate (500/day), Unlimited (unlimited) 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ToolsApi.new
url = 'url_example' # String | TikTok video URL or ID
opts = {
  action: 'download', # String | 'formats' to list available formats
  format_id: 'format_id_example' # String | Specific format ID (0 = no watermark, etc.)
}

begin
  # Download TikTok video
  result = api_instance.download_tik_tok_video(url, opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling ToolsApi->download_tik_tok_video: #{e}"
end
```

#### Using the download_tik_tok_video_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DownloadTikTokVideo200Response>, Integer, Hash)> download_tik_tok_video_with_http_info(url, opts)

```ruby
begin
  # Download TikTok video
  data, status_code, headers = api_instance.download_tik_tok_video_with_http_info(url, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DownloadTikTokVideo200Response>
rescue Late::ApiError => e
  puts "Error when calling ToolsApi->download_tik_tok_video_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | TikTok video URL or ID |  |
| **action** | **String** | &#39;formats&#39; to list available formats | [optional][default to &#39;download&#39;] |
| **format_id** | **String** | Specific format ID (0 &#x3D; no watermark, etc.) | [optional] |

### Return type

[**DownloadTikTokVideo200Response**](DownloadTikTokVideo200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## download_twitter_media

> <DownloadInstagramMedia200Response> download_twitter_media(url, opts)

Download Twitter/X video

Download videos from Twitter/X posts.  **Rate Limits:** Build (50/day), Accelerate (500/day), Unlimited (unlimited) 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ToolsApi.new
url = 'https://x.com/user/status/123456789' # String | Twitter/X post URL
opts = {
  action: 'download', # String | 
  format_id: 'format_id_example' # String | 
}

begin
  # Download Twitter/X video
  result = api_instance.download_twitter_media(url, opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling ToolsApi->download_twitter_media: #{e}"
end
```

#### Using the download_twitter_media_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DownloadInstagramMedia200Response>, Integer, Hash)> download_twitter_media_with_http_info(url, opts)

```ruby
begin
  # Download Twitter/X video
  data, status_code, headers = api_instance.download_twitter_media_with_http_info(url, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DownloadInstagramMedia200Response>
rescue Late::ApiError => e
  puts "Error when calling ToolsApi->download_twitter_media_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | Twitter/X post URL |  |
| **action** | **String** |  | [optional][default to &#39;download&#39;] |
| **format_id** | **String** |  | [optional] |

### Return type

[**DownloadInstagramMedia200Response**](DownloadInstagramMedia200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## download_you_tube_video

> <DownloadYouTubeVideo200Response> download_you_tube_video(url, opts)

Download YouTube video or audio

Download YouTube videos or audio. Returns available formats or direct download URL.  **Rate Limits:** Build (50/day), Accelerate (500/day), Unlimited (unlimited) 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ToolsApi.new
url = 'https://www.youtube.com/watch?v=dQw4w9WgXcQ' # String | YouTube video URL or video ID
opts = {
  action: 'download', # String | Action to perform: 'download' returns download URL, 'formats' lists available formats
  format: 'video', # String | Desired format (when action=download)
  quality: 'hd', # String | Desired quality (when action=download)
  format_id: 'format_id_example' # String | Specific format ID from formats list
}

begin
  # Download YouTube video or audio
  result = api_instance.download_you_tube_video(url, opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling ToolsApi->download_you_tube_video: #{e}"
end
```

#### Using the download_you_tube_video_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DownloadYouTubeVideo200Response>, Integer, Hash)> download_you_tube_video_with_http_info(url, opts)

```ruby
begin
  # Download YouTube video or audio
  data, status_code, headers = api_instance.download_you_tube_video_with_http_info(url, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DownloadYouTubeVideo200Response>
rescue Late::ApiError => e
  puts "Error when calling ToolsApi->download_you_tube_video_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | YouTube video URL or video ID |  |
| **action** | **String** | Action to perform: &#39;download&#39; returns download URL, &#39;formats&#39; lists available formats | [optional][default to &#39;download&#39;] |
| **format** | **String** | Desired format (when action&#x3D;download) | [optional][default to &#39;video&#39;] |
| **quality** | **String** | Desired quality (when action&#x3D;download) | [optional][default to &#39;hd&#39;] |
| **format_id** | **String** | Specific format ID from formats list | [optional] |

### Return type

[**DownloadYouTubeVideo200Response**](DownloadYouTubeVideo200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_you_tube_transcript

> <GetYouTubeTranscript200Response> get_you_tube_transcript(url, opts)

Get YouTube video transcript

Extract transcript/captions from a YouTube video.  **Rate Limits:** Build (50/day), Accelerate (500/day), Unlimited (unlimited) 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ToolsApi.new
url = 'url_example' # String | YouTube video URL or video ID
opts = {
  lang: 'lang_example' # String | Language code for transcript
}

begin
  # Get YouTube video transcript
  result = api_instance.get_you_tube_transcript(url, opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling ToolsApi->get_you_tube_transcript: #{e}"
end
```

#### Using the get_you_tube_transcript_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetYouTubeTranscript200Response>, Integer, Hash)> get_you_tube_transcript_with_http_info(url, opts)

```ruby
begin
  # Get YouTube video transcript
  data, status_code, headers = api_instance.get_you_tube_transcript_with_http_info(url, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetYouTubeTranscript200Response>
rescue Late::ApiError => e
  puts "Error when calling ToolsApi->get_you_tube_transcript_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | YouTube video URL or video ID |  |
| **lang** | **String** | Language code for transcript | [optional][default to &#39;en&#39;] |

### Return type

[**GetYouTubeTranscript200Response**](GetYouTubeTranscript200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

