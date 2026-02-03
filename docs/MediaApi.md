# Late::MediaApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_media_presigned_url**](MediaApi.md#get_media_presigned_url) | **POST** /v1/media/presign | Get a presigned URL for direct file upload (up to 5GB) |


## get_media_presigned_url

> <GetMediaPresignedUrl200Response> get_media_presigned_url(get_media_presigned_url_request)

Get a presigned URL for direct file upload (up to 5GB)

Get a presigned URL to upload files directly to cloud storage. This is the recommended method for uploading files of any size, especially files larger than ~4MB.  **How it works:** 1. Call this endpoint with the filename and content type 2. Receive an `uploadUrl` (presigned) and `publicUrl` 3. PUT your file directly to the `uploadUrl` 4. Use the `publicUrl` in your posts  **Benefits:** - Supports files up to 5GB - Files upload directly to storage (faster, no server bottleneck) - No 413 errors from server body size limits  **Example:** ```javascript // Step 1: Get presigned URL const response = await fetch('https://getlate.dev/api/v1/media/presign', {   method: 'POST',   headers: {     'Authorization': 'Bearer YOUR_API_KEY',     'Content-Type': 'application/json'   },   body: JSON.stringify({     filename: 'my-video.mp4',     contentType: 'video/mp4'   }) }); const { uploadUrl, publicUrl } = await response.json();  // Step 2: Upload file directly to storage await fetch(uploadUrl, {   method: 'PUT',   body: file,   headers: { 'Content-Type': 'video/mp4' } });  // Step 3: Use publicUrl when creating your post // The publicUrl is ready to use immediately after upload completes ``` 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::MediaApi.new
get_media_presigned_url_request = Late::GetMediaPresignedUrlRequest.new({filename: 'my-video.mp4', content_type: 'image/jpeg'}) # GetMediaPresignedUrlRequest | 

begin
  # Get a presigned URL for direct file upload (up to 5GB)
  result = api_instance.get_media_presigned_url(get_media_presigned_url_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling MediaApi->get_media_presigned_url: #{e}"
end
```

#### Using the get_media_presigned_url_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetMediaPresignedUrl200Response>, Integer, Hash)> get_media_presigned_url_with_http_info(get_media_presigned_url_request)

```ruby
begin
  # Get a presigned URL for direct file upload (up to 5GB)
  data, status_code, headers = api_instance.get_media_presigned_url_with_http_info(get_media_presigned_url_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetMediaPresignedUrl200Response>
rescue Late::ApiError => e
  puts "Error when calling MediaApi->get_media_presigned_url_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **get_media_presigned_url_request** | [**GetMediaPresignedUrlRequest**](GetMediaPresignedUrlRequest.md) |  |  |

### Return type

[**GetMediaPresignedUrl200Response**](GetMediaPresignedUrl200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

