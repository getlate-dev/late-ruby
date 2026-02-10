# Late::LogsApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_log**](LogsApi.md#get_log) | **GET** /v1/logs/{logId} | Get a single log entry |
| [**get_post_logs**](LogsApi.md#get_post_logs) | **GET** /v1/posts/{postId}/logs | Get logs for a specific post |
| [**list_connection_logs**](LogsApi.md#list_connection_logs) | **GET** /v1/connections/logs | Get connection logs |
| [**list_logs**](LogsApi.md#list_logs) | **GET** /v1/logs | Get publishing logs (deprecated) |
| [**list_posts_logs**](LogsApi.md#list_posts_logs) | **GET** /v1/posts/logs | Get publishing logs |


## get_log

> <GetLog200Response> get_log(log_id)

Get a single log entry

Retrieve detailed information about a specific log entry, including full request and response bodies for debugging. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::LogsApi.new
log_id = 'log_id_example' # String | The log entry ID

begin
  # Get a single log entry
  result = api_instance.get_log(log_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling LogsApi->get_log: #{e}"
end
```

#### Using the get_log_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetLog200Response>, Integer, Hash)> get_log_with_http_info(log_id)

```ruby
begin
  # Get a single log entry
  data, status_code, headers = api_instance.get_log_with_http_info(log_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetLog200Response>
rescue Late::ApiError => e
  puts "Error when calling LogsApi->get_log_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **log_id** | **String** | The log entry ID |  |

### Return type

[**GetLog200Response**](GetLog200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_post_logs

> <GetPostLogs200Response> get_post_logs(post_id, opts)

Get logs for a specific post

Retrieve all publishing logs for a specific post. Shows the complete history of publishing attempts for that post across all platforms. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::LogsApi.new
post_id = 'post_id_example' # String | The post ID
opts = {
  limit: 56 # Integer | Maximum number of logs to return (max 100)
}

begin
  # Get logs for a specific post
  result = api_instance.get_post_logs(post_id, opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling LogsApi->get_post_logs: #{e}"
end
```

#### Using the get_post_logs_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetPostLogs200Response>, Integer, Hash)> get_post_logs_with_http_info(post_id, opts)

```ruby
begin
  # Get logs for a specific post
  data, status_code, headers = api_instance.get_post_logs_with_http_info(post_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetPostLogs200Response>
rescue Late::ApiError => e
  puts "Error when calling LogsApi->get_post_logs_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_id** | **String** | The post ID |  |
| **limit** | **Integer** | Maximum number of logs to return (max 100) | [optional][default to 50] |

### Return type

[**GetPostLogs200Response**](GetPostLogs200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_connection_logs

> <ListConnectionLogs200Response> list_connection_logs(opts)

Get connection logs

Retrieve connection event logs showing account connection and disconnection history. Useful for debugging OAuth issues and tracking account lifecycle.  **Event Types:** - `connect_success` - New account connected successfully - `connect_failed` - Connection attempt failed - `disconnect` - Account was disconnected - `reconnect_success` - Existing account reconnected - `reconnect_failed` - Reconnection attempt failed  **Retention:** Logs are automatically deleted after 7 days. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::LogsApi.new
opts = {
  platform: 'tiktok', # String | Filter by platform
  event_type: 'connect_success', # String | Filter by event type
  status: 'success', # String | Filter by status (shorthand for event types)
  days: 56, # Integer | Number of days to look back (max 7)
  limit: 56, # Integer | Maximum number of logs to return (max 100)
  skip: 56 # Integer | Number of logs to skip (for pagination)
}

begin
  # Get connection logs
  result = api_instance.list_connection_logs(opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling LogsApi->list_connection_logs: #{e}"
end
```

#### Using the list_connection_logs_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListConnectionLogs200Response>, Integer, Hash)> list_connection_logs_with_http_info(opts)

```ruby
begin
  # Get connection logs
  data, status_code, headers = api_instance.list_connection_logs_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListConnectionLogs200Response>
rescue Late::ApiError => e
  puts "Error when calling LogsApi->list_connection_logs_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **platform** | **String** | Filter by platform | [optional] |
| **event_type** | **String** | Filter by event type | [optional] |
| **status** | **String** | Filter by status (shorthand for event types) | [optional] |
| **days** | **Integer** | Number of days to look back (max 7) | [optional][default to 7] |
| **limit** | **Integer** | Maximum number of logs to return (max 100) | [optional][default to 50] |
| **skip** | **Integer** | Number of logs to skip (for pagination) | [optional][default to 0] |

### Return type

[**ListConnectionLogs200Response**](ListConnectionLogs200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_logs

> <ListLogs200Response> list_logs(opts)

Get publishing logs (deprecated)

**Deprecated:** Use `/v1/posts/logs` instead. This endpoint is maintained for backwards compatibility.  Retrieve publishing logs for all posts. Logs show detailed information about each publishing attempt including API requests, responses, and timing data.  **Filtering:** - Filter by status (success, failed, pending, skipped) - Filter by platform (instagram, twitter, linkedin, etc.) - Filter by action (publish, retry, rate_limit_pause, etc.)  **Retention:** Logs are automatically deleted after 7 days. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::LogsApi.new
opts = {
  status: 'success', # String | Filter by log status
  platform: 'tiktok', # String | Filter by platform
  action: 'publish', # String | Filter by action type
  days: 56, # Integer | Number of days to look back (max 7)
  limit: 56, # Integer | Maximum number of logs to return (max 100)
  skip: 56 # Integer | Number of logs to skip (for pagination)
}

begin
  # Get publishing logs (deprecated)
  result = api_instance.list_logs(opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling LogsApi->list_logs: #{e}"
end
```

#### Using the list_logs_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListLogs200Response>, Integer, Hash)> list_logs_with_http_info(opts)

```ruby
begin
  # Get publishing logs (deprecated)
  data, status_code, headers = api_instance.list_logs_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListLogs200Response>
rescue Late::ApiError => e
  puts "Error when calling LogsApi->list_logs_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** | Filter by log status | [optional] |
| **platform** | **String** | Filter by platform | [optional] |
| **action** | **String** | Filter by action type | [optional] |
| **days** | **Integer** | Number of days to look back (max 7) | [optional][default to 7] |
| **limit** | **Integer** | Maximum number of logs to return (max 100) | [optional][default to 50] |
| **skip** | **Integer** | Number of logs to skip (for pagination) | [optional][default to 0] |

### Return type

[**ListLogs200Response**](ListLogs200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_posts_logs

> <ListLogs200Response> list_posts_logs(opts)

Get publishing logs

Retrieve publishing logs for all posts. Logs show detailed information about each publishing attempt including API requests, responses, and timing data.  **Filtering:** - Filter by status (success, failed, pending, skipped) - Filter by platform (instagram, twitter, linkedin, etc.) - Filter by action (publish, retry, rate_limit_pause, etc.)  **Retention:** Logs are automatically deleted after 7 days. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::LogsApi.new
opts = {
  status: 'success', # String | Filter by log status
  platform: 'tiktok', # String | Filter by platform
  action: 'publish', # String | Filter by action type
  days: 56, # Integer | Number of days to look back (max 7)
  limit: 56, # Integer | Maximum number of logs to return (max 100)
  skip: 56 # Integer | Number of logs to skip (for pagination)
}

begin
  # Get publishing logs
  result = api_instance.list_posts_logs(opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling LogsApi->list_posts_logs: #{e}"
end
```

#### Using the list_posts_logs_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListLogs200Response>, Integer, Hash)> list_posts_logs_with_http_info(opts)

```ruby
begin
  # Get publishing logs
  data, status_code, headers = api_instance.list_posts_logs_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListLogs200Response>
rescue Late::ApiError => e
  puts "Error when calling LogsApi->list_posts_logs_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** | Filter by log status | [optional] |
| **platform** | **String** | Filter by platform | [optional] |
| **action** | **String** | Filter by action type | [optional] |
| **days** | **Integer** | Number of days to look back (max 7) | [optional][default to 7] |
| **limit** | **Integer** | Maximum number of logs to return (max 100) | [optional][default to 50] |
| **skip** | **Integer** | Number of logs to skip (for pagination) | [optional][default to 0] |

### Return type

[**ListLogs200Response**](ListLogs200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

