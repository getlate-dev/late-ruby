# Late::GMBMediaApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_google_business_media**](GMBMediaApi.md#create_google_business_media) | **POST** /v1/accounts/{accountId}/gmb-media | Upload a photo to Google Business Profile |
| [**delete_google_business_media**](GMBMediaApi.md#delete_google_business_media) | **DELETE** /v1/accounts/{accountId}/gmb-media | Delete a photo from Google Business Profile |
| [**list_google_business_media**](GMBMediaApi.md#list_google_business_media) | **GET** /v1/accounts/{accountId}/gmb-media | List Google Business Profile media (photos) |


## create_google_business_media

> <CreateGoogleBusinessMedia200Response> create_google_business_media(account_id, create_google_business_media_request)

Upload a photo to Google Business Profile

Creates a media item (photo) for a location from a publicly accessible URL.  Categories determine where the photo appears: - `COVER` - Cover photo - `PROFILE` - Profile photo - `LOGO` - Business logo - `EXTERIOR` - Exterior shots - `INTERIOR` - Interior shots - `FOOD_AND_DRINK` - Food and drink photos - `MENU` - Menu photos - `PRODUCT` - Product photos - `TEAMS` - Team/staff photos - `ADDITIONAL` - Other photos 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::GMBMediaApi.new
account_id = 'account_id_example' # String | 
create_google_business_media_request = Late::CreateGoogleBusinessMediaRequest.new({source_url: 'source_url_example'}) # CreateGoogleBusinessMediaRequest | 

begin
  # Upload a photo to Google Business Profile
  result = api_instance.create_google_business_media(account_id, create_google_business_media_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling GMBMediaApi->create_google_business_media: #{e}"
end
```

#### Using the create_google_business_media_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateGoogleBusinessMedia200Response>, Integer, Hash)> create_google_business_media_with_http_info(account_id, create_google_business_media_request)

```ruby
begin
  # Upload a photo to Google Business Profile
  data, status_code, headers = api_instance.create_google_business_media_with_http_info(account_id, create_google_business_media_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateGoogleBusinessMedia200Response>
rescue Late::ApiError => e
  puts "Error when calling GMBMediaApi->create_google_business_media_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |
| **create_google_business_media_request** | [**CreateGoogleBusinessMediaRequest**](CreateGoogleBusinessMediaRequest.md) |  |  |

### Return type

[**CreateGoogleBusinessMedia200Response**](CreateGoogleBusinessMedia200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_google_business_media

> <DeleteGoogleBusinessMedia200Response> delete_google_business_media(account_id, media_id)

Delete a photo from Google Business Profile

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::GMBMediaApi.new
account_id = 'account_id_example' # String | 
media_id = 'media_id_example' # String | The media item ID to delete

begin
  # Delete a photo from Google Business Profile
  result = api_instance.delete_google_business_media(account_id, media_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling GMBMediaApi->delete_google_business_media: #{e}"
end
```

#### Using the delete_google_business_media_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeleteGoogleBusinessMedia200Response>, Integer, Hash)> delete_google_business_media_with_http_info(account_id, media_id)

```ruby
begin
  # Delete a photo from Google Business Profile
  data, status_code, headers = api_instance.delete_google_business_media_with_http_info(account_id, media_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeleteGoogleBusinessMedia200Response>
rescue Late::ApiError => e
  puts "Error when calling GMBMediaApi->delete_google_business_media_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |
| **media_id** | **String** | The media item ID to delete |  |

### Return type

[**DeleteGoogleBusinessMedia200Response**](DeleteGoogleBusinessMedia200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_google_business_media

> <ListGoogleBusinessMedia200Response> list_google_business_media(account_id, opts)

List Google Business Profile media (photos)

Lists media items (photos) for a Google Business Profile location. Returns photo URLs, descriptions, categories, and metadata. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::GMBMediaApi.new
account_id = 'account_id_example' # String | 
opts = {
  page_size: 56, # Integer | Number of items to return (max 100)
  page_token: 'page_token_example' # String | Pagination token from previous response
}

begin
  # List Google Business Profile media (photos)
  result = api_instance.list_google_business_media(account_id, opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling GMBMediaApi->list_google_business_media: #{e}"
end
```

#### Using the list_google_business_media_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListGoogleBusinessMedia200Response>, Integer, Hash)> list_google_business_media_with_http_info(account_id, opts)

```ruby
begin
  # List Google Business Profile media (photos)
  data, status_code, headers = api_instance.list_google_business_media_with_http_info(account_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListGoogleBusinessMedia200Response>
rescue Late::ApiError => e
  puts "Error when calling GMBMediaApi->list_google_business_media_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |
| **page_size** | **Integer** | Number of items to return (max 100) | [optional][default to 100] |
| **page_token** | **String** | Pagination token from previous response | [optional] |

### Return type

[**ListGoogleBusinessMedia200Response**](ListGoogleBusinessMedia200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

