# Late::AccountGroupsApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_account_group**](AccountGroupsApi.md#create_account_group) | **POST** /v1/account-groups | Create group |
| [**delete_account_group**](AccountGroupsApi.md#delete_account_group) | **DELETE** /v1/account-groups/{groupId} | Delete group |
| [**list_account_groups**](AccountGroupsApi.md#list_account_groups) | **GET** /v1/account-groups | List groups |
| [**update_account_group**](AccountGroupsApi.md#update_account_group) | **PUT** /v1/account-groups/{groupId} | Update group |


## create_account_group

> <CreateAccountGroup201Response> create_account_group(create_account_group_request)

Create group

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::AccountGroupsApi.new
create_account_group_request = Late::CreateAccountGroupRequest.new({name: 'name_example', account_ids: ['account_ids_example']}) # CreateAccountGroupRequest | 

begin
  # Create group
  result = api_instance.create_account_group(create_account_group_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling AccountGroupsApi->create_account_group: #{e}"
end
```

#### Using the create_account_group_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateAccountGroup201Response>, Integer, Hash)> create_account_group_with_http_info(create_account_group_request)

```ruby
begin
  # Create group
  data, status_code, headers = api_instance.create_account_group_with_http_info(create_account_group_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateAccountGroup201Response>
rescue Late::ApiError => e
  puts "Error when calling AccountGroupsApi->create_account_group_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_account_group_request** | [**CreateAccountGroupRequest**](CreateAccountGroupRequest.md) |  |  |

### Return type

[**CreateAccountGroup201Response**](CreateAccountGroup201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_account_group

> <DeleteAccountGroup200Response> delete_account_group(group_id)

Delete group

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::AccountGroupsApi.new
group_id = 'group_id_example' # String | 

begin
  # Delete group
  result = api_instance.delete_account_group(group_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling AccountGroupsApi->delete_account_group: #{e}"
end
```

#### Using the delete_account_group_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeleteAccountGroup200Response>, Integer, Hash)> delete_account_group_with_http_info(group_id)

```ruby
begin
  # Delete group
  data, status_code, headers = api_instance.delete_account_group_with_http_info(group_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeleteAccountGroup200Response>
rescue Late::ApiError => e
  puts "Error when calling AccountGroupsApi->delete_account_group_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **group_id** | **String** |  |  |

### Return type

[**DeleteAccountGroup200Response**](DeleteAccountGroup200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_account_groups

> <ListAccountGroups200Response> list_account_groups

List groups

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::AccountGroupsApi.new

begin
  # List groups
  result = api_instance.list_account_groups
  p result
rescue Late::ApiError => e
  puts "Error when calling AccountGroupsApi->list_account_groups: #{e}"
end
```

#### Using the list_account_groups_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListAccountGroups200Response>, Integer, Hash)> list_account_groups_with_http_info

```ruby
begin
  # List groups
  data, status_code, headers = api_instance.list_account_groups_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListAccountGroups200Response>
rescue Late::ApiError => e
  puts "Error when calling AccountGroupsApi->list_account_groups_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**ListAccountGroups200Response**](ListAccountGroups200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_account_group

> <UpdateAccountGroup200Response> update_account_group(group_id, update_account_group_request)

Update group

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::AccountGroupsApi.new
group_id = 'group_id_example' # String | 
update_account_group_request = Late::UpdateAccountGroupRequest.new # UpdateAccountGroupRequest | 

begin
  # Update group
  result = api_instance.update_account_group(group_id, update_account_group_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling AccountGroupsApi->update_account_group: #{e}"
end
```

#### Using the update_account_group_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UpdateAccountGroup200Response>, Integer, Hash)> update_account_group_with_http_info(group_id, update_account_group_request)

```ruby
begin
  # Update group
  data, status_code, headers = api_instance.update_account_group_with_http_info(group_id, update_account_group_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UpdateAccountGroup200Response>
rescue Late::ApiError => e
  puts "Error when calling AccountGroupsApi->update_account_group_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **group_id** | **String** |  |  |
| **update_account_group_request** | [**UpdateAccountGroupRequest**](UpdateAccountGroupRequest.md) |  |  |

### Return type

[**UpdateAccountGroup200Response**](UpdateAccountGroup200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

