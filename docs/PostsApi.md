# Late::PostsApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**bulk_upload_posts**](PostsApi.md#bulk_upload_posts) | **POST** /v1/posts/bulk-upload | Bulk upload from CSV |
| [**create_post**](PostsApi.md#create_post) | **POST** /v1/posts | Create post |
| [**delete_post**](PostsApi.md#delete_post) | **DELETE** /v1/posts/{postId} | Delete post |
| [**get_post**](PostsApi.md#get_post) | **GET** /v1/posts/{postId} | Get post |
| [**list_posts**](PostsApi.md#list_posts) | **GET** /v1/posts | List posts |
| [**retry_post**](PostsApi.md#retry_post) | **POST** /v1/posts/{postId}/retry | Retry failed post |
| [**unpublish_post**](PostsApi.md#unpublish_post) | **POST** /v1/posts/{postId}/unpublish | Unpublish post |
| [**update_post**](PostsApi.md#update_post) | **PUT** /v1/posts/{postId} | Update post |


## bulk_upload_posts

> <BulkUploadPosts200Response> bulk_upload_posts(opts)

Bulk upload from CSV

Create multiple posts by uploading a CSV file. Use dryRun=true to validate without creating posts.

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
  # Bulk upload from CSV
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
  # Bulk upload from CSV
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

Create post

Create and optionally publish a post. Immediate posts (publishNow: true) include platformPostUrl in the response. Content is optional when media is attached or all platforms have customContent. See each platform's schema for media constraints. 

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
  # Create post
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
  # Create post
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

Delete post

Delete a draft or scheduled post from Late. Published posts cannot be deleted; use the Unpublish endpoint instead. Upload quota is automatically refunded.

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
  # Delete post
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
  # Delete post
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

Get post

Fetch a single post by ID. For published posts, this returns platformPostUrl for each platform. 

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
  # Get post
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
  # Get post
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

List posts

Returns a paginated list of posts. Published posts include platformPostUrl with the public URL on each platform.

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
  # List posts
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
  # List posts
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

Retry failed post

Immediately retries publishing a failed post. Returns the updated post with its new status.

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
  # Retry failed post
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
  # Retry failed post
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


## unpublish_post

> <UnpublishPost200Response> unpublish_post(post_id, unpublish_post_request)

Unpublish post

Deletes a published post from the specified platform. The post record in Late is kept but its status is updated to cancelled. Not supported on Instagram, TikTok, or Snapchat. Threaded posts delete all items. YouTube deletion is permanent. 

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
unpublish_post_request = Late::UnpublishPostRequest.new({platform: 'threads'}) # UnpublishPostRequest | 

begin
  # Unpublish post
  result = api_instance.unpublish_post(post_id, unpublish_post_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling PostsApi->unpublish_post: #{e}"
end
```

#### Using the unpublish_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UnpublishPost200Response>, Integer, Hash)> unpublish_post_with_http_info(post_id, unpublish_post_request)

```ruby
begin
  # Unpublish post
  data, status_code, headers = api_instance.unpublish_post_with_http_info(post_id, unpublish_post_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UnpublishPost200Response>
rescue Late::ApiError => e
  puts "Error when calling PostsApi->unpublish_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_id** | **String** |  |  |
| **unpublish_post_request** | [**UnpublishPostRequest**](UnpublishPostRequest.md) |  |  |

### Return type

[**UnpublishPost200Response**](UnpublishPost200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_post

> <PostUpdateResponse> update_post(post_id, update_post_request)

Update post

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
  # Update post
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
  # Update post
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

