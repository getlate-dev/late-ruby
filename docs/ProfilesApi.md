# Late::ProfilesApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_profile**](ProfilesApi.md#create_profile) | **POST** /v1/profiles | Create profile |
| [**delete_profile**](ProfilesApi.md#delete_profile) | **DELETE** /v1/profiles/{profileId} | Delete profile |
| [**get_profile**](ProfilesApi.md#get_profile) | **GET** /v1/profiles/{profileId} | Get profile |
| [**list_profiles**](ProfilesApi.md#list_profiles) | **GET** /v1/profiles | List profiles |
| [**update_profile**](ProfilesApi.md#update_profile) | **PUT** /v1/profiles/{profileId} | Update profile |


## create_profile

> <ProfileCreateResponse> create_profile(create_profile_request)

Create profile

Creates a new profile with a name, optional description, and color.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ProfilesApi.new
create_profile_request = Late::CreateProfileRequest.new({name: 'name_example'}) # CreateProfileRequest | 

begin
  # Create profile
  result = api_instance.create_profile(create_profile_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling ProfilesApi->create_profile: #{e}"
end
```

#### Using the create_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ProfileCreateResponse>, Integer, Hash)> create_profile_with_http_info(create_profile_request)

```ruby
begin
  # Create profile
  data, status_code, headers = api_instance.create_profile_with_http_info(create_profile_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ProfileCreateResponse>
rescue Late::ApiError => e
  puts "Error when calling ProfilesApi->create_profile_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_profile_request** | [**CreateProfileRequest**](CreateProfileRequest.md) |  |  |

### Return type

[**ProfileCreateResponse**](ProfileCreateResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_profile

> <DeleteAccountGroup200Response> delete_profile(profile_id)

Delete profile

Permanently deletes a profile by ID.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ProfilesApi.new
profile_id = 'profile_id_example' # String | 

begin
  # Delete profile
  result = api_instance.delete_profile(profile_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling ProfilesApi->delete_profile: #{e}"
end
```

#### Using the delete_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeleteAccountGroup200Response>, Integer, Hash)> delete_profile_with_http_info(profile_id)

```ruby
begin
  # Delete profile
  data, status_code, headers = api_instance.delete_profile_with_http_info(profile_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeleteAccountGroup200Response>
rescue Late::ApiError => e
  puts "Error when calling ProfilesApi->delete_profile_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** |  |  |

### Return type

[**DeleteAccountGroup200Response**](DeleteAccountGroup200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_profile

> <GetProfile200Response> get_profile(profile_id)

Get profile

Returns a single profile by ID, including its name, color, and default status.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ProfilesApi.new
profile_id = 'profile_id_example' # String | 

begin
  # Get profile
  result = api_instance.get_profile(profile_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling ProfilesApi->get_profile: #{e}"
end
```

#### Using the get_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetProfile200Response>, Integer, Hash)> get_profile_with_http_info(profile_id)

```ruby
begin
  # Get profile
  data, status_code, headers = api_instance.get_profile_with_http_info(profile_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetProfile200Response>
rescue Late::ApiError => e
  puts "Error when calling ProfilesApi->get_profile_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** |  |  |

### Return type

[**GetProfile200Response**](GetProfile200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_profiles

> <ProfilesListResponse> list_profiles(opts)

List profiles

Returns profiles sorted by creation date. Use includeOverLimit=true to include profiles that exceed the plan limit.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ProfilesApi.new
opts = {
  include_over_limit: true # Boolean | When true, includes over-limit profiles (marked with isOverLimit: true).
}

begin
  # List profiles
  result = api_instance.list_profiles(opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling ProfilesApi->list_profiles: #{e}"
end
```

#### Using the list_profiles_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ProfilesListResponse>, Integer, Hash)> list_profiles_with_http_info(opts)

```ruby
begin
  # List profiles
  data, status_code, headers = api_instance.list_profiles_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ProfilesListResponse>
rescue Late::ApiError => e
  puts "Error when calling ProfilesApi->list_profiles_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **include_over_limit** | **Boolean** | When true, includes over-limit profiles (marked with isOverLimit: true). | [optional][default to false] |

### Return type

[**ProfilesListResponse**](ProfilesListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_profile

> <UpdateProfile200Response> update_profile(profile_id, update_profile_request)

Update profile

Updates a profile's name, description, color, or default status.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ProfilesApi.new
profile_id = 'profile_id_example' # String | 
update_profile_request = Late::UpdateProfileRequest.new # UpdateProfileRequest | 

begin
  # Update profile
  result = api_instance.update_profile(profile_id, update_profile_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling ProfilesApi->update_profile: #{e}"
end
```

#### Using the update_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UpdateProfile200Response>, Integer, Hash)> update_profile_with_http_info(profile_id, update_profile_request)

```ruby
begin
  # Update profile
  data, status_code, headers = api_instance.update_profile_with_http_info(profile_id, update_profile_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UpdateProfile200Response>
rescue Late::ApiError => e
  puts "Error when calling ProfilesApi->update_profile_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** |  |  |
| **update_profile_request** | [**UpdateProfileRequest**](UpdateProfileRequest.md) |  |  |

### Return type

[**UpdateProfile200Response**](UpdateProfile200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

