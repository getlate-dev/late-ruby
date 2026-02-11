# Late::PostsApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**bulk_upload_posts**](PostsApi.md#bulk_upload_posts) | **POST** /v1/posts/bulk-upload | Validate and schedule multiple posts from CSV |
| [**create_post**](PostsApi.md#create_post) | **POST** /v1/posts | Create a draft, scheduled, or immediate post |
| [**delete_post**](PostsApi.md#delete_post) | **DELETE** /v1/posts/{postId} | Delete a post |
| [**get_post**](PostsApi.md#get_post) | **GET** /v1/posts/{postId} | Get a single post |
| [**list_posts**](PostsApi.md#list_posts) | **GET** /v1/posts | List posts visible to the authenticated user |
| [**retry_post**](PostsApi.md#retry_post) | **POST** /v1/posts/{postId}/retry | Retry publishing a failed or partial post |
| [**update_post**](PostsApi.md#update_post) | **PUT** /v1/posts/{postId} | Update a post |


## bulk_upload_posts

> <BulkUploadPosts200Response> bulk_upload_posts(opts)

Validate and schedule multiple posts from CSV

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::PostsApi.new
opts = {
  dry_run: true, # Boolean | 
  file: File.new('/path/to/some/file') # File | 
}

begin
  # Validate and schedule multiple posts from CSV
  result = api_instance.bulk_upload_posts(opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling PostsApi->bulk_upload_posts: #{e}"
end
```

#### Using the bulk_upload_posts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BulkUploadPosts200Response>, Integer, Hash)> bulk_upload_posts_with_http_info(opts)

```ruby
begin
  # Validate and schedule multiple posts from CSV
  data, status_code, headers = api_instance.bulk_upload_posts_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BulkUploadPosts200Response>
rescue Late::ApiError => e
  puts "Error when calling PostsApi->bulk_upload_posts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **dry_run** | **Boolean** |  | [optional][default to false] |
| **file** | **File** |  | [optional] |

### Return type

[**BulkUploadPosts200Response**](BulkUploadPosts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json


## create_post

> <PostCreateResponse> create_post(create_post_request)

Create a draft, scheduled, or immediate post

**Getting Post URLs:** - For immediate posts (`publishNow: true`): The response includes `platformPostUrl` in each platform entry under `post.platforms[]`. - For scheduled posts: Fetch the post via `GET /v1/posts/{postId}` after the scheduled time; `platformPostUrl` will be populated once published.  **Content/Caption requirements:** - `content` (caption/description) is optional when:   - Media is attached (`mediaItems` or per-platform `customMedia`)   - All platforms have `customContent` set   - Posting only to YouTube (title is used instead) - Text-only posts (no media) require `content` - Stories do not use captions (content is ignored) - Reels, feed posts, and other media posts can have optional captions  Platform constraints: - YouTube requires a video in mediaItems; optional custom thumbnail via MediaItem.thumbnail. - Instagram and TikTok require media; do not mix videos and images for TikTok. - Instagram carousels support up to 10 items; Stories publish as 'story'. - Threads carousels support up to 10 images (no videos in carousels); single posts support one image or video. - Facebook Stories require media (single image or video); set contentType to 'story' in platformSpecificData. - LinkedIn multi-image supports up to 20 images; single PDF documents supported (max 100MB, ~300 pages, cannot mix with other media). - Pinterest supports single image via image_url or a single video per Pin; boardId is required. - Bluesky supports up to 4 images per post. Images may be automatically recompressed to ≤ ~1MB to satisfy Bluesky's blob limit. When no media is attached, a link preview may be generated for URLs in the text. - Snapchat requires media (single image or video); set contentType to 'story', 'saved_story', or 'spotlight' in platformSpecificData. Stories are ephemeral (24h), Saved Stories are permanent, Spotlight is for video content.  **Multi-page/multi-location posting:** Some platforms allow posting to multiple pages, organizations, or locations from a single account connection. Use the same accountId multiple times with different targets in platformSpecificData: - Facebook: `pageId` - post to multiple Facebook Pages (list via GET /v1/accounts/{id}/facebook-page) - LinkedIn: `organizationUrn` - post to multiple organizations (list via GET /v1/accounts/{id}/linkedin-organizations) - Google Business: `locationId` - post to multiple locations (list via GET /v1/accounts/{id}/gmb-locations) - Reddit: `subreddit` - post to multiple subreddits from the same account 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::PostsApi.new
create_post_request = Late::CreatePostRequest.new # CreatePostRequest | 

begin
  # Create a draft, scheduled, or immediate post
  result = api_instance.create_post(create_post_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling PostsApi->create_post: #{e}"
end
```

#### Using the create_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PostCreateResponse>, Integer, Hash)> create_post_with_http_info(create_post_request)

```ruby
begin
  # Create a draft, scheduled, or immediate post
  data, status_code, headers = api_instance.create_post_with_http_info(create_post_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PostCreateResponse>
rescue Late::ApiError => e
  puts "Error when calling PostsApi->create_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_post_request** | [**CreatePostRequest**](CreatePostRequest.md) |  |  |

### Return type

[**PostCreateResponse**](PostCreateResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_post

> <PostDeleteResponse> delete_post(post_id)

Delete a post

Delete a post. Published posts cannot be deleted.  When deleting a scheduled or draft post that consumed upload quota, the quota will be automatically refunded. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::PostsApi.new
post_id = 'post_id_example' # String | 

begin
  # Delete a post
  result = api_instance.delete_post(post_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling PostsApi->delete_post: #{e}"
end
```

#### Using the delete_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PostDeleteResponse>, Integer, Hash)> delete_post_with_http_info(post_id)

```ruby
begin
  # Delete a post
  data, status_code, headers = api_instance.delete_post_with_http_info(post_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PostDeleteResponse>
rescue Late::ApiError => e
  puts "Error when calling PostsApi->delete_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_id** | **String** |  |  |

### Return type

[**PostDeleteResponse**](PostDeleteResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_post

> <PostGetResponse> get_post(post_id)

Get a single post

Fetch a single post by ID. For published posts, this returns `platformPostUrl`  for each platform - useful for retrieving post URLs after scheduled posts publish. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::PostsApi.new
post_id = 'post_id_example' # String | 

begin
  # Get a single post
  result = api_instance.get_post(post_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling PostsApi->get_post: #{e}"
end
```

#### Using the get_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PostGetResponse>, Integer, Hash)> get_post_with_http_info(post_id)

```ruby
begin
  # Get a single post
  data, status_code, headers = api_instance.get_post_with_http_info(post_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PostGetResponse>
rescue Late::ApiError => e
  puts "Error when calling PostsApi->get_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_id** | **String** |  |  |

### Return type

[**PostGetResponse**](PostGetResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_posts

> <PostsListResponse> list_posts(opts)

List posts visible to the authenticated user

**Getting Post URLs:** For published posts, each platform entry includes `platformPostUrl` with the public URL. Use `status=published` filter to fetch only published posts with their URLs.  Notes and constraints by platform when interpreting the response: - YouTube: posts always include at least one video in mediaItems. - Instagram/TikTok: posts always include media; drafts may omit media until finalized in client. - TikTok: mediaItems will not mix photos and videos in the same post. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::PostsApi.new
opts = {
  page: 56, # Integer | Page number (1-based)
  limit: 56, # Integer | Page size
  status: 'draft', # String | 
  platform: 'twitter', # String | 
  profile_id: 'profile_id_example', # String | 
  created_by: 'created_by_example', # String | 
  date_from: Date.parse('2013-10-20'), # Date | 
  date_to: Date.parse('2013-10-20'), # Date | 
  include_hidden: true # Boolean | 
}

begin
  # List posts visible to the authenticated user
  result = api_instance.list_posts(opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling PostsApi->list_posts: #{e}"
end
```

#### Using the list_posts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PostsListResponse>, Integer, Hash)> list_posts_with_http_info(opts)

```ruby
begin
  # List posts visible to the authenticated user
  data, status_code, headers = api_instance.list_posts_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PostsListResponse>
rescue Late::ApiError => e
  puts "Error when calling PostsApi->list_posts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** | Page number (1-based) | [optional][default to 1] |
| **limit** | **Integer** | Page size | [optional][default to 10] |
| **status** | **String** |  | [optional] |
| **platform** | **String** |  | [optional] |
| **profile_id** | **String** |  | [optional] |
| **created_by** | **String** |  | [optional] |
| **date_from** | **Date** |  | [optional] |
| **date_to** | **Date** |  | [optional] |
| **include_hidden** | **Boolean** |  | [optional][default to false] |

### Return type

[**PostsListResponse**](PostsListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## retry_post

> <PostRetryResponse> retry_post(post_id)

Retry publishing a failed or partial post

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::PostsApi.new
post_id = 'post_id_example' # String | 

begin
  # Retry publishing a failed or partial post
  result = api_instance.retry_post(post_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling PostsApi->retry_post: #{e}"
end
```

#### Using the retry_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PostRetryResponse>, Integer, Hash)> retry_post_with_http_info(post_id)

```ruby
begin
  # Retry publishing a failed or partial post
  data, status_code, headers = api_instance.retry_post_with_http_info(post_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PostRetryResponse>
rescue Late::ApiError => e
  puts "Error when calling PostsApi->retry_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_id** | **String** |  |  |

### Return type

[**PostRetryResponse**](PostRetryResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_post

> <PostUpdateResponse> update_post(post_id, update_post_request)

Update a post

Update an existing post. Only draft, scheduled, failed, and partial posts can be edited. Published, publishing, and cancelled posts cannot be modified. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::PostsApi.new
post_id = 'post_id_example' # String | 
update_post_request = Late::UpdatePostRequest.new # UpdatePostRequest | 

begin
  # Update a post
  result = api_instance.update_post(post_id, update_post_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling PostsApi->update_post: #{e}"
end
```

#### Using the update_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PostUpdateResponse>, Integer, Hash)> update_post_with_http_info(post_id, update_post_request)

```ruby
begin
  # Update a post
  data, status_code, headers = api_instance.update_post_with_http_info(post_id, update_post_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PostUpdateResponse>
rescue Late::ApiError => e
  puts "Error when calling PostsApi->update_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_id** | **String** |  |  |
| **update_post_request** | [**UpdatePostRequest**](UpdatePostRequest.md) |  |  |

### Return type

[**PostUpdateResponse**](PostUpdateResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

