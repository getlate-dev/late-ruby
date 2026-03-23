# Late::SequencesApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**activate_sequence**](SequencesApi.md#activate_sequence) | **POST** /v1/sequences/{sequenceId}/activate | Activate a sequence |
| [**create_sequence**](SequencesApi.md#create_sequence) | **POST** /v1/sequences | Create a sequence |
| [**delete_sequence**](SequencesApi.md#delete_sequence) | **DELETE** /v1/sequences/{sequenceId} | Delete a sequence |
| [**enroll_contacts**](SequencesApi.md#enroll_contacts) | **POST** /v1/sequences/{sequenceId}/enroll | Enroll contacts in a sequence |
| [**get_sequence**](SequencesApi.md#get_sequence) | **GET** /v1/sequences/{sequenceId} | Get sequence with steps |
| [**list_sequence_enrollments**](SequencesApi.md#list_sequence_enrollments) | **GET** /v1/sequences/{sequenceId}/enrollments | List enrollments for a sequence |
| [**list_sequences**](SequencesApi.md#list_sequences) | **GET** /v1/sequences | List sequences |
| [**pause_sequence**](SequencesApi.md#pause_sequence) | **POST** /v1/sequences/{sequenceId}/pause | Pause a sequence |
| [**unenroll_contact**](SequencesApi.md#unenroll_contact) | **DELETE** /v1/sequences/{sequenceId}/enroll/{contactId} | Unenroll a contact from a sequence |
| [**update_sequence**](SequencesApi.md#update_sequence) | **PATCH** /v1/sequences/{sequenceId} | Update a sequence |


## activate_sequence

> activate_sequence(sequence_id)

Activate a sequence

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::SequencesApi.new
sequence_id = 'sequence_id_example' # String | 

begin
  # Activate a sequence
  api_instance.activate_sequence(sequence_id)
rescue Late::ApiError => e
  puts "Error when calling SequencesApi->activate_sequence: #{e}"
end
```

#### Using the activate_sequence_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> activate_sequence_with_http_info(sequence_id)

```ruby
begin
  # Activate a sequence
  data, status_code, headers = api_instance.activate_sequence_with_http_info(sequence_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Late::ApiError => e
  puts "Error when calling SequencesApi->activate_sequence_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sequence_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## create_sequence

> create_sequence(create_sequence_request)

Create a sequence

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::SequencesApi.new
create_sequence_request = Late::CreateSequenceRequest.new({profile_id: 'profile_id_example', account_id: 'account_id_example', platform: 'instagram', name: 'name_example'}) # CreateSequenceRequest | 

begin
  # Create a sequence
  api_instance.create_sequence(create_sequence_request)
rescue Late::ApiError => e
  puts "Error when calling SequencesApi->create_sequence: #{e}"
end
```

#### Using the create_sequence_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> create_sequence_with_http_info(create_sequence_request)

```ruby
begin
  # Create a sequence
  data, status_code, headers = api_instance.create_sequence_with_http_info(create_sequence_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Late::ApiError => e
  puts "Error when calling SequencesApi->create_sequence_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_sequence_request** | [**CreateSequenceRequest**](CreateSequenceRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_sequence

> delete_sequence(sequence_id)

Delete a sequence

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::SequencesApi.new
sequence_id = 'sequence_id_example' # String | 

begin
  # Delete a sequence
  api_instance.delete_sequence(sequence_id)
rescue Late::ApiError => e
  puts "Error when calling SequencesApi->delete_sequence: #{e}"
end
```

#### Using the delete_sequence_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_sequence_with_http_info(sequence_id)

```ruby
begin
  # Delete a sequence
  data, status_code, headers = api_instance.delete_sequence_with_http_info(sequence_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Late::ApiError => e
  puts "Error when calling SequencesApi->delete_sequence_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sequence_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## enroll_contacts

> enroll_contacts(sequence_id, enroll_contacts_request)

Enroll contacts in a sequence

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::SequencesApi.new
sequence_id = 'sequence_id_example' # String | 
enroll_contacts_request = Late::EnrollContactsRequest.new({contact_ids: ['contact_ids_example']}) # EnrollContactsRequest | 

begin
  # Enroll contacts in a sequence
  api_instance.enroll_contacts(sequence_id, enroll_contacts_request)
rescue Late::ApiError => e
  puts "Error when calling SequencesApi->enroll_contacts: #{e}"
end
```

#### Using the enroll_contacts_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> enroll_contacts_with_http_info(sequence_id, enroll_contacts_request)

```ruby
begin
  # Enroll contacts in a sequence
  data, status_code, headers = api_instance.enroll_contacts_with_http_info(sequence_id, enroll_contacts_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Late::ApiError => e
  puts "Error when calling SequencesApi->enroll_contacts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sequence_id** | **String** |  |  |
| **enroll_contacts_request** | [**EnrollContactsRequest**](EnrollContactsRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## get_sequence

> get_sequence(sequence_id)

Get sequence with steps

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::SequencesApi.new
sequence_id = 'sequence_id_example' # String | 

begin
  # Get sequence with steps
  api_instance.get_sequence(sequence_id)
rescue Late::ApiError => e
  puts "Error when calling SequencesApi->get_sequence: #{e}"
end
```

#### Using the get_sequence_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> get_sequence_with_http_info(sequence_id)

```ruby
begin
  # Get sequence with steps
  data, status_code, headers = api_instance.get_sequence_with_http_info(sequence_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Late::ApiError => e
  puts "Error when calling SequencesApi->get_sequence_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sequence_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_sequence_enrollments

> list_sequence_enrollments(sequence_id, opts)

List enrollments for a sequence

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::SequencesApi.new
sequence_id = 'sequence_id_example' # String | 
opts = {
  status: 'active', # String | 
  limit: 56, # Integer | 
  skip: 56 # Integer | 
}

begin
  # List enrollments for a sequence
  api_instance.list_sequence_enrollments(sequence_id, opts)
rescue Late::ApiError => e
  puts "Error when calling SequencesApi->list_sequence_enrollments: #{e}"
end
```

#### Using the list_sequence_enrollments_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> list_sequence_enrollments_with_http_info(sequence_id, opts)

```ruby
begin
  # List enrollments for a sequence
  data, status_code, headers = api_instance.list_sequence_enrollments_with_http_info(sequence_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Late::ApiError => e
  puts "Error when calling SequencesApi->list_sequence_enrollments_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sequence_id** | **String** |  |  |
| **status** | **String** |  | [optional] |
| **limit** | **Integer** |  | [optional][default to 50] |
| **skip** | **Integer** |  | [optional][default to 0] |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_sequences

> list_sequences(opts)

List sequences

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::SequencesApi.new
opts = {
  profile_id: 'profile_id_example', # String | Filter by profile. Omit to list across all profiles
  status: 'draft', # String | 
  limit: 56, # Integer | 
  skip: 56 # Integer | 
}

begin
  # List sequences
  api_instance.list_sequences(opts)
rescue Late::ApiError => e
  puts "Error when calling SequencesApi->list_sequences: #{e}"
end
```

#### Using the list_sequences_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> list_sequences_with_http_info(opts)

```ruby
begin
  # List sequences
  data, status_code, headers = api_instance.list_sequences_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Late::ApiError => e
  puts "Error when calling SequencesApi->list_sequences_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** | Filter by profile. Omit to list across all profiles | [optional] |
| **status** | **String** |  | [optional] |
| **limit** | **Integer** |  | [optional][default to 50] |
| **skip** | **Integer** |  | [optional][default to 0] |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## pause_sequence

> pause_sequence(sequence_id)

Pause a sequence

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::SequencesApi.new
sequence_id = 'sequence_id_example' # String | 

begin
  # Pause a sequence
  api_instance.pause_sequence(sequence_id)
rescue Late::ApiError => e
  puts "Error when calling SequencesApi->pause_sequence: #{e}"
end
```

#### Using the pause_sequence_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> pause_sequence_with_http_info(sequence_id)

```ruby
begin
  # Pause a sequence
  data, status_code, headers = api_instance.pause_sequence_with_http_info(sequence_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Late::ApiError => e
  puts "Error when calling SequencesApi->pause_sequence_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sequence_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## unenroll_contact

> unenroll_contact(sequence_id, contact_id)

Unenroll a contact from a sequence

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::SequencesApi.new
sequence_id = 'sequence_id_example' # String | 
contact_id = 'contact_id_example' # String | 

begin
  # Unenroll a contact from a sequence
  api_instance.unenroll_contact(sequence_id, contact_id)
rescue Late::ApiError => e
  puts "Error when calling SequencesApi->unenroll_contact: #{e}"
end
```

#### Using the unenroll_contact_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> unenroll_contact_with_http_info(sequence_id, contact_id)

```ruby
begin
  # Unenroll a contact from a sequence
  data, status_code, headers = api_instance.unenroll_contact_with_http_info(sequence_id, contact_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Late::ApiError => e
  puts "Error when calling SequencesApi->unenroll_contact_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sequence_id** | **String** |  |  |
| **contact_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_sequence

> update_sequence(sequence_id)

Update a sequence

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::SequencesApi.new
sequence_id = 'sequence_id_example' # String | 

begin
  # Update a sequence
  api_instance.update_sequence(sequence_id)
rescue Late::ApiError => e
  puts "Error when calling SequencesApi->update_sequence: #{e}"
end
```

#### Using the update_sequence_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> update_sequence_with_http_info(sequence_id)

```ruby
begin
  # Update a sequence
  data, status_code, headers = api_instance.update_sequence_with_http_info(sequence_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Late::ApiError => e
  puts "Error when calling SequencesApi->update_sequence_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sequence_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

