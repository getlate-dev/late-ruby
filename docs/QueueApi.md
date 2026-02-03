# Late::QueueApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_queue_slot**](QueueApi.md#create_queue_slot) | **POST** /v1/queue/slots | Create a new queue for a profile |
| [**delete_queue_slot**](QueueApi.md#delete_queue_slot) | **DELETE** /v1/queue/slots | Delete a queue schedule |
| [**get_next_queue_slot**](QueueApi.md#get_next_queue_slot) | **GET** /v1/queue/next-slot | Preview the next available queue slot (informational only) |
| [**list_queue_slots**](QueueApi.md#list_queue_slots) | **GET** /v1/queue/slots | Get queue schedules for a profile |
| [**preview_queue**](QueueApi.md#preview_queue) | **GET** /v1/queue/preview | Preview upcoming queue slots for a profile |
| [**update_queue_slot**](QueueApi.md#update_queue_slot) | **PUT** /v1/queue/slots | Create or update a queue schedule |


## create_queue_slot

> <CreateQueueSlot201Response> create_queue_slot(create_queue_slot_request)

Create a new queue for a profile

Create an additional queue for a profile. The first queue created becomes the default. Subsequent queues are non-default unless explicitly set. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::QueueApi.new
create_queue_slot_request = Late::CreateQueueSlotRequest.new({profile_id: 'profile_id_example', name: 'name_example', timezone: 'timezone_example', slots: [Late::QueueSlot.new]}) # CreateQueueSlotRequest | 

begin
  # Create a new queue for a profile
  result = api_instance.create_queue_slot(create_queue_slot_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling QueueApi->create_queue_slot: #{e}"
end
```

#### Using the create_queue_slot_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateQueueSlot201Response>, Integer, Hash)> create_queue_slot_with_http_info(create_queue_slot_request)

```ruby
begin
  # Create a new queue for a profile
  data, status_code, headers = api_instance.create_queue_slot_with_http_info(create_queue_slot_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateQueueSlot201Response>
rescue Late::ApiError => e
  puts "Error when calling QueueApi->create_queue_slot_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_queue_slot_request** | [**CreateQueueSlotRequest**](CreateQueueSlotRequest.md) |  |  |

### Return type

[**CreateQueueSlot201Response**](CreateQueueSlot201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_queue_slot

> <DeleteQueueSlot200Response> delete_queue_slot(profile_id, queue_id)

Delete a queue schedule

Delete a queue from a profile. Requires queueId to specify which queue to delete. If deleting the default queue, another queue will be promoted to default. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::QueueApi.new
profile_id = 'profile_id_example' # String | 
queue_id = 'queue_id_example' # String | Queue ID to delete

begin
  # Delete a queue schedule
  result = api_instance.delete_queue_slot(profile_id, queue_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling QueueApi->delete_queue_slot: #{e}"
end
```

#### Using the delete_queue_slot_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeleteQueueSlot200Response>, Integer, Hash)> delete_queue_slot_with_http_info(profile_id, queue_id)

```ruby
begin
  # Delete a queue schedule
  data, status_code, headers = api_instance.delete_queue_slot_with_http_info(profile_id, queue_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeleteQueueSlot200Response>
rescue Late::ApiError => e
  puts "Error when calling QueueApi->delete_queue_slot_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** |  |  |
| **queue_id** | **String** | Queue ID to delete |  |

### Return type

[**DeleteQueueSlot200Response**](DeleteQueueSlot200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_next_queue_slot

> <GetNextQueueSlot200Response> get_next_queue_slot(profile_id, opts)

Preview the next available queue slot (informational only)

Returns the next available queue slot for preview/informational purposes.  **Important: To schedule a post to the queue, do NOT use this endpoint's response with `scheduledFor`.** That creates a manual post, not a queue post.  Instead, use `POST /v1/posts` with `queuedFromProfile` (and optionally `queueId`). The system will automatically assign the next available slot with proper locking to prevent race conditions.  This endpoint is useful for: - Showing users when their next post will go out before they commit - Debugging/verifying queue configuration - Building UI previews  If no queueId is specified, uses the profile's default queue. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::QueueApi.new
profile_id = 'profile_id_example' # String | 
opts = {
  queue_id: 'queue_id_example' # String | Specific queue ID (optional, defaults to profile's default queue)
}

begin
  # Preview the next available queue slot (informational only)
  result = api_instance.get_next_queue_slot(profile_id, opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling QueueApi->get_next_queue_slot: #{e}"
end
```

#### Using the get_next_queue_slot_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetNextQueueSlot200Response>, Integer, Hash)> get_next_queue_slot_with_http_info(profile_id, opts)

```ruby
begin
  # Preview the next available queue slot (informational only)
  data, status_code, headers = api_instance.get_next_queue_slot_with_http_info(profile_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetNextQueueSlot200Response>
rescue Late::ApiError => e
  puts "Error when calling QueueApi->get_next_queue_slot_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** |  |  |
| **queue_id** | **String** | Specific queue ID (optional, defaults to profile&#39;s default queue) | [optional] |

### Return type

[**GetNextQueueSlot200Response**](GetNextQueueSlot200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_queue_slots

> <ListQueueSlots200Response> list_queue_slots(profile_id, opts)

Get queue schedules for a profile

Retrieve queue schedules for a profile. Each profile can have multiple queues. - Without `all=true`: Returns the default queue (or specific queue if queueId provided) - With `all=true`: Returns all queues for the profile 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::QueueApi.new
profile_id = 'profile_id_example' # String | Profile ID to get queues for
opts = {
  queue_id: 'queue_id_example', # String | Specific queue ID to retrieve (optional)
  all: 'true' # String | Set to 'true' to list all queues for the profile
}

begin
  # Get queue schedules for a profile
  result = api_instance.list_queue_slots(profile_id, opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling QueueApi->list_queue_slots: #{e}"
end
```

#### Using the list_queue_slots_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListQueueSlots200Response>, Integer, Hash)> list_queue_slots_with_http_info(profile_id, opts)

```ruby
begin
  # Get queue schedules for a profile
  data, status_code, headers = api_instance.list_queue_slots_with_http_info(profile_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListQueueSlots200Response>
rescue Late::ApiError => e
  puts "Error when calling QueueApi->list_queue_slots_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** | Profile ID to get queues for |  |
| **queue_id** | **String** | Specific queue ID to retrieve (optional) | [optional] |
| **all** | **String** | Set to &#39;true&#39; to list all queues for the profile | [optional] |

### Return type

[**ListQueueSlots200Response**](ListQueueSlots200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## preview_queue

> <PreviewQueue200Response> preview_queue(profile_id, opts)

Preview upcoming queue slots for a profile

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::QueueApi.new
profile_id = 'profile_id_example' # String | 
opts = {
  count: 56 # Integer | 
}

begin
  # Preview upcoming queue slots for a profile
  result = api_instance.preview_queue(profile_id, opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling QueueApi->preview_queue: #{e}"
end
```

#### Using the preview_queue_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PreviewQueue200Response>, Integer, Hash)> preview_queue_with_http_info(profile_id, opts)

```ruby
begin
  # Preview upcoming queue slots for a profile
  data, status_code, headers = api_instance.preview_queue_with_http_info(profile_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PreviewQueue200Response>
rescue Late::ApiError => e
  puts "Error when calling QueueApi->preview_queue_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** |  |  |
| **count** | **Integer** |  | [optional][default to 20] |

### Return type

[**PreviewQueue200Response**](PreviewQueue200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_queue_slot

> <UpdateQueueSlot200Response> update_queue_slot(update_queue_slot_request)

Create or update a queue schedule

Create a new queue or update an existing one. - Without queueId: Creates or updates the default queue - With queueId: Updates the specific queue - With setAsDefault=true: Makes this queue the default for the profile 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::QueueApi.new
update_queue_slot_request = Late::UpdateQueueSlotRequest.new({profile_id: 'profile_id_example', timezone: 'timezone_example', slots: [Late::QueueSlot.new]}) # UpdateQueueSlotRequest | 

begin
  # Create or update a queue schedule
  result = api_instance.update_queue_slot(update_queue_slot_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling QueueApi->update_queue_slot: #{e}"
end
```

#### Using the update_queue_slot_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UpdateQueueSlot200Response>, Integer, Hash)> update_queue_slot_with_http_info(update_queue_slot_request)

```ruby
begin
  # Create or update a queue schedule
  data, status_code, headers = api_instance.update_queue_slot_with_http_info(update_queue_slot_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UpdateQueueSlot200Response>
rescue Late::ApiError => e
  puts "Error when calling QueueApi->update_queue_slot_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **update_queue_slot_request** | [**UpdateQueueSlotRequest**](UpdateQueueSlotRequest.md) |  |  |

### Return type

[**UpdateQueueSlot200Response**](UpdateQueueSlot200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

