# Late::ContactsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**bulk_create_contacts**](ContactsApi.md#bulk_create_contacts) | **POST** /v1/contacts/bulk | Bulk create contacts |
| [**create_contact**](ContactsApi.md#create_contact) | **POST** /v1/contacts | Create a contact |
| [**delete_contact**](ContactsApi.md#delete_contact) | **DELETE** /v1/contacts/{contactId} | Delete a contact |
| [**get_contact**](ContactsApi.md#get_contact) | **GET** /v1/contacts/{contactId} | Get contact with channels |
| [**get_contact_channels**](ContactsApi.md#get_contact_channels) | **GET** /v1/contacts/{contactId}/channels | List channels for a contact |
| [**list_contacts**](ContactsApi.md#list_contacts) | **GET** /v1/contacts | List contacts |
| [**update_contact**](ContactsApi.md#update_contact) | **PATCH** /v1/contacts/{contactId} | Update a contact |


## bulk_create_contacts

> bulk_create_contacts(bulk_create_contacts_request)

Bulk create contacts

Import up to 1000 contacts at a time. Skips duplicates.

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ContactsApi.new
bulk_create_contacts_request = Late::BulkCreateContactsRequest.new({profile_id: 'profile_id_example', account_id: 'account_id_example', platform: 'platform_example', contacts: [Late::BulkCreateContactsRequestContactsInner.new({name: 'name_example', platform_identifier: 'platform_identifier_example'})]}) # BulkCreateContactsRequest | 

begin
  # Bulk create contacts
  api_instance.bulk_create_contacts(bulk_create_contacts_request)
rescue Late::ApiError => e
  puts "Error when calling ContactsApi->bulk_create_contacts: #{e}"
end
```

#### Using the bulk_create_contacts_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> bulk_create_contacts_with_http_info(bulk_create_contacts_request)

```ruby
begin
  # Bulk create contacts
  data, status_code, headers = api_instance.bulk_create_contacts_with_http_info(bulk_create_contacts_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Late::ApiError => e
  puts "Error when calling ContactsApi->bulk_create_contacts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **bulk_create_contacts_request** | [**BulkCreateContactsRequest**](BulkCreateContactsRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_contact

> create_contact(create_contact_request)

Create a contact

Create a new contact. Optionally create a platform channel in the same request by providing accountId, platform, and platformIdentifier.

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ContactsApi.new
create_contact_request = Late::CreateContactRequest.new({profile_id: 'profile_id_example', name: 'name_example'}) # CreateContactRequest | 

begin
  # Create a contact
  api_instance.create_contact(create_contact_request)
rescue Late::ApiError => e
  puts "Error when calling ContactsApi->create_contact: #{e}"
end
```

#### Using the create_contact_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> create_contact_with_http_info(create_contact_request)

```ruby
begin
  # Create a contact
  data, status_code, headers = api_instance.create_contact_with_http_info(create_contact_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Late::ApiError => e
  puts "Error when calling ContactsApi->create_contact_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_contact_request** | [**CreateContactRequest**](CreateContactRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_contact

> delete_contact(contact_id)

Delete a contact

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ContactsApi.new
contact_id = 'contact_id_example' # String | 

begin
  # Delete a contact
  api_instance.delete_contact(contact_id)
rescue Late::ApiError => e
  puts "Error when calling ContactsApi->delete_contact: #{e}"
end
```

#### Using the delete_contact_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_contact_with_http_info(contact_id)

```ruby
begin
  # Delete a contact
  data, status_code, headers = api_instance.delete_contact_with_http_info(contact_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Late::ApiError => e
  puts "Error when calling ContactsApi->delete_contact_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **contact_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_contact

> get_contact(contact_id)

Get contact with channels

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ContactsApi.new
contact_id = 'contact_id_example' # String | 

begin
  # Get contact with channels
  api_instance.get_contact(contact_id)
rescue Late::ApiError => e
  puts "Error when calling ContactsApi->get_contact: #{e}"
end
```

#### Using the get_contact_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> get_contact_with_http_info(contact_id)

```ruby
begin
  # Get contact with channels
  data, status_code, headers = api_instance.get_contact_with_http_info(contact_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Late::ApiError => e
  puts "Error when calling ContactsApi->get_contact_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **contact_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_contact_channels

> get_contact_channels(contact_id)

List channels for a contact

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ContactsApi.new
contact_id = 'contact_id_example' # String | 

begin
  # List channels for a contact
  api_instance.get_contact_channels(contact_id)
rescue Late::ApiError => e
  puts "Error when calling ContactsApi->get_contact_channels: #{e}"
end
```

#### Using the get_contact_channels_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> get_contact_channels_with_http_info(contact_id)

```ruby
begin
  # List channels for a contact
  data, status_code, headers = api_instance.get_contact_channels_with_http_info(contact_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Late::ApiError => e
  puts "Error when calling ContactsApi->get_contact_channels_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **contact_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_contacts

> list_contacts(opts)

List contacts

List and search contacts for a profile. Supports filtering by tags, platform, subscription status, and full-text search.

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ContactsApi.new
opts = {
  profile_id: 'profile_id_example', # String | Filter by profile. Omit to list across all profiles
  search: 'search_example', # String | 
  tag: 'tag_example', # String | 
  platform: 'instagram', # String | 
  is_subscribed: 'true', # String | 
  limit: 56, # Integer | 
  skip: 56 # Integer | 
}

begin
  # List contacts
  api_instance.list_contacts(opts)
rescue Late::ApiError => e
  puts "Error when calling ContactsApi->list_contacts: #{e}"
end
```

#### Using the list_contacts_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> list_contacts_with_http_info(opts)

```ruby
begin
  # List contacts
  data, status_code, headers = api_instance.list_contacts_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Late::ApiError => e
  puts "Error when calling ContactsApi->list_contacts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** | Filter by profile. Omit to list across all profiles | [optional] |
| **search** | **String** |  | [optional] |
| **tag** | **String** |  | [optional] |
| **platform** | **String** |  | [optional] |
| **is_subscribed** | **String** |  | [optional] |
| **limit** | **Integer** |  | [optional][default to 50] |
| **skip** | **Integer** |  | [optional][default to 0] |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_contact

> update_contact(contact_id, opts)

Update a contact

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::ContactsApi.new
contact_id = 'contact_id_example' # String | 
opts = {
  update_contact_request: Late::UpdateContactRequest.new # UpdateContactRequest | 
}

begin
  # Update a contact
  api_instance.update_contact(contact_id, opts)
rescue Late::ApiError => e
  puts "Error when calling ContactsApi->update_contact: #{e}"
end
```

#### Using the update_contact_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> update_contact_with_http_info(contact_id, opts)

```ruby
begin
  # Update a contact
  data, status_code, headers = api_instance.update_contact_with_http_info(contact_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Late::ApiError => e
  puts "Error when calling ContactsApi->update_contact_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **contact_id** | **String** |  |  |
| **update_contact_request** | [**UpdateContactRequest**](UpdateContactRequest.md) |  | [optional] |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

