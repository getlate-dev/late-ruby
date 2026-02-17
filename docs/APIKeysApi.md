# Late::APIKeysApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_api_key**](APIKeysApi.md#create_api_key) | **POST** /v1/api-keys | Create key |
| [**delete_api_key**](APIKeysApi.md#delete_api_key) | **DELETE** /v1/api-keys/{keyId} | Delete key |
| [**list_api_keys**](APIKeysApi.md#list_api_keys) | **GET** /v1/api-keys | List keys |


## create_api_key

> <CreateApiKey201Response> create_api_key(create_api_key_request)

Create key

Creates a new API key with an optional expiry. The full key value is only returned once in the response.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::APIKeysApi.new
create_api_key_request = Late::CreateApiKeyRequest.new({name: 'name_example'}) # CreateApiKeyRequest | 

begin
  # Create key
  result = api_instance.create_api_key(create_api_key_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling APIKeysApi->create_api_key: #{e}"
end
```

#### Using the create_api_key_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateApiKey201Response>, Integer, Hash)> create_api_key_with_http_info(create_api_key_request)

```ruby
begin
  # Create key
  data, status_code, headers = api_instance.create_api_key_with_http_info(create_api_key_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateApiKey201Response>
rescue Late::ApiError => e
  puts "Error when calling APIKeysApi->create_api_key_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_api_key_request** | [**CreateApiKeyRequest**](CreateApiKeyRequest.md) |  |  |

### Return type

[**CreateApiKey201Response**](CreateApiKey201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_api_key

> <DeleteAccountGroup200Response> delete_api_key(key_id)

Delete key

Permanently revokes and deletes an API key.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::APIKeysApi.new
key_id = 'key_id_example' # String | 

begin
  # Delete key
  result = api_instance.delete_api_key(key_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling APIKeysApi->delete_api_key: #{e}"
end
```

#### Using the delete_api_key_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeleteAccountGroup200Response>, Integer, Hash)> delete_api_key_with_http_info(key_id)

```ruby
begin
  # Delete key
  data, status_code, headers = api_instance.delete_api_key_with_http_info(key_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeleteAccountGroup200Response>
rescue Late::ApiError => e
  puts "Error when calling APIKeysApi->delete_api_key_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **key_id** | **String** |  |  |

### Return type

[**DeleteAccountGroup200Response**](DeleteAccountGroup200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_api_keys

> <ListApiKeys200Response> list_api_keys

List keys

Returns all API keys for the authenticated user. Keys are returned with a preview only, not the full key value.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::APIKeysApi.new

begin
  # List keys
  result = api_instance.list_api_keys
  p result
rescue Late::ApiError => e
  puts "Error when calling APIKeysApi->list_api_keys: #{e}"
end
```

#### Using the list_api_keys_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListApiKeys200Response>, Integer, Hash)> list_api_keys_with_http_info

```ruby
begin
  # List keys
  data, status_code, headers = api_instance.list_api_keys_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListApiKeys200Response>
rescue Late::ApiError => e
  puts "Error when calling APIKeysApi->list_api_keys_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**ListApiKeys200Response**](ListApiKeys200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

