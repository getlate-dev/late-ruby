# Late::MediaApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_media_presigned_url**](MediaApi.md#get_media_presigned_url) | **POST** /v1/media/presign | Get presigned upload URL |


## get_media_presigned_url

> <GetMediaPresignedUrl200Response> get_media_presigned_url(get_media_presigned_url_request)

Get presigned upload URL

Get a presigned URL to upload files directly to cloud storage. Supports files up to 5GB.  How it works: call this endpoint with the filename and content type, receive an uploadUrl (presigned) and publicUrl, PUT your file directly to the uploadUrl, then use the publicUrl in your posts. 

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
  # Get presigned upload URL
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
  # Get presigned upload URL
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

