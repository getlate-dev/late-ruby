# Late::CommentAutomationsApi

All URIs are relative to *https://zernio.com/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_comment_automation**](CommentAutomationsApi.md#create_comment_automation) | **POST** /v1/comment-automations | Create a comment-to-DM automation |
| [**delete_comment_automation**](CommentAutomationsApi.md#delete_comment_automation) | **DELETE** /v1/comment-automations/{automationId} | Delete automation and all logs |
| [**get_comment_automation**](CommentAutomationsApi.md#get_comment_automation) | **GET** /v1/comment-automations/{automationId} | Get automation details with recent logs |
| [**list_comment_automation_logs**](CommentAutomationsApi.md#list_comment_automation_logs) | **GET** /v1/comment-automations/{automationId}/logs | List trigger logs for an automation |
| [**list_comment_automations**](CommentAutomationsApi.md#list_comment_automations) | **GET** /v1/comment-automations | List comment-to-DM automations |
| [**update_comment_automation**](CommentAutomationsApi.md#update_comment_automation) | **PATCH** /v1/comment-automations/{automationId} | Update automation settings |


## create_comment_automation

> <CreateCommentAutomation200Response> create_comment_automation(create_comment_automation_request)

Create a comment-to-DM automation

Create a keyword-triggered DM automation on an Instagram or Facebook post. When someone comments a matching keyword, they automatically receive a DM. Only one active automation per post is allowed. 

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::CommentAutomationsApi.new
create_comment_automation_request = Late::CreateCommentAutomationRequest.new({profile_id: 'profile_id_example', account_id: 'account_id_example', platform_post_id: 'platform_post_id_example', name: 'name_example', dm_message: 'dm_message_example'}) # CreateCommentAutomationRequest | 

begin
  # Create a comment-to-DM automation
  result = api_instance.create_comment_automation(create_comment_automation_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling CommentAutomationsApi->create_comment_automation: #{e}"
end
```

#### Using the create_comment_automation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateCommentAutomation200Response>, Integer, Hash)> create_comment_automation_with_http_info(create_comment_automation_request)

```ruby
begin
  # Create a comment-to-DM automation
  data, status_code, headers = api_instance.create_comment_automation_with_http_info(create_comment_automation_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateCommentAutomation200Response>
rescue Late::ApiError => e
  puts "Error when calling CommentAutomationsApi->create_comment_automation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_comment_automation_request** | [**CreateCommentAutomationRequest**](CreateCommentAutomationRequest.md) |  |  |

### Return type

[**CreateCommentAutomation200Response**](CreateCommentAutomation200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_comment_automation

> delete_comment_automation(automation_id)

Delete automation and all logs

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::CommentAutomationsApi.new
automation_id = 'automation_id_example' # String | 

begin
  # Delete automation and all logs
  api_instance.delete_comment_automation(automation_id)
rescue Late::ApiError => e
  puts "Error when calling CommentAutomationsApi->delete_comment_automation: #{e}"
end
```

#### Using the delete_comment_automation_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_comment_automation_with_http_info(automation_id)

```ruby
begin
  # Delete automation and all logs
  data, status_code, headers = api_instance.delete_comment_automation_with_http_info(automation_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Late::ApiError => e
  puts "Error when calling CommentAutomationsApi->delete_comment_automation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **automation_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_comment_automation

> <GetCommentAutomation200Response> get_comment_automation(automation_id)

Get automation details with recent logs

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::CommentAutomationsApi.new
automation_id = 'automation_id_example' # String | 

begin
  # Get automation details with recent logs
  result = api_instance.get_comment_automation(automation_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling CommentAutomationsApi->get_comment_automation: #{e}"
end
```

#### Using the get_comment_automation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetCommentAutomation200Response>, Integer, Hash)> get_comment_automation_with_http_info(automation_id)

```ruby
begin
  # Get automation details with recent logs
  data, status_code, headers = api_instance.get_comment_automation_with_http_info(automation_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetCommentAutomation200Response>
rescue Late::ApiError => e
  puts "Error when calling CommentAutomationsApi->get_comment_automation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **automation_id** | **String** |  |  |

### Return type

[**GetCommentAutomation200Response**](GetCommentAutomation200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_comment_automation_logs

> <ListCommentAutomationLogs200Response> list_comment_automation_logs(automation_id, opts)

List trigger logs for an automation

Paginated list of every comment that triggered this automation, with send status and commenter info.

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::CommentAutomationsApi.new
automation_id = 'automation_id_example' # String | 
opts = {
  status: 'sent', # String | Filter by result status
  limit: 56, # Integer | 
  skip: 56 # Integer | 
}

begin
  # List trigger logs for an automation
  result = api_instance.list_comment_automation_logs(automation_id, opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling CommentAutomationsApi->list_comment_automation_logs: #{e}"
end
```

#### Using the list_comment_automation_logs_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListCommentAutomationLogs200Response>, Integer, Hash)> list_comment_automation_logs_with_http_info(automation_id, opts)

```ruby
begin
  # List trigger logs for an automation
  data, status_code, headers = api_instance.list_comment_automation_logs_with_http_info(automation_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListCommentAutomationLogs200Response>
rescue Late::ApiError => e
  puts "Error when calling CommentAutomationsApi->list_comment_automation_logs_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **automation_id** | **String** |  |  |
| **status** | **String** | Filter by result status | [optional] |
| **limit** | **Integer** |  | [optional][default to 50] |
| **skip** | **Integer** |  | [optional][default to 0] |

### Return type

[**ListCommentAutomationLogs200Response**](ListCommentAutomationLogs200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_comment_automations

> <ListCommentAutomations200Response> list_comment_automations(opts)

List comment-to-DM automations

List all comment-to-DM automations for a profile. Returns automations with their stats.

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::CommentAutomationsApi.new
opts = {
  profile_id: 'profile_id_example' # String | Filter by profile. Omit to list across all profiles
}

begin
  # List comment-to-DM automations
  result = api_instance.list_comment_automations(opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling CommentAutomationsApi->list_comment_automations: #{e}"
end
```

#### Using the list_comment_automations_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListCommentAutomations200Response>, Integer, Hash)> list_comment_automations_with_http_info(opts)

```ruby
begin
  # List comment-to-DM automations
  data, status_code, headers = api_instance.list_comment_automations_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListCommentAutomations200Response>
rescue Late::ApiError => e
  puts "Error when calling CommentAutomationsApi->list_comment_automations_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** | Filter by profile. Omit to list across all profiles | [optional] |

### Return type

[**ListCommentAutomations200Response**](ListCommentAutomations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_comment_automation

> <UpdateCommentAutomation200Response> update_comment_automation(automation_id, opts)

Update automation settings

### Examples

```ruby
require 'time'
require 'late-sdk'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::CommentAutomationsApi.new
automation_id = 'automation_id_example' # String | 
opts = {
  update_comment_automation_request: Late::UpdateCommentAutomationRequest.new # UpdateCommentAutomationRequest | 
}

begin
  # Update automation settings
  result = api_instance.update_comment_automation(automation_id, opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling CommentAutomationsApi->update_comment_automation: #{e}"
end
```

#### Using the update_comment_automation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UpdateCommentAutomation200Response>, Integer, Hash)> update_comment_automation_with_http_info(automation_id, opts)

```ruby
begin
  # Update automation settings
  data, status_code, headers = api_instance.update_comment_automation_with_http_info(automation_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UpdateCommentAutomation200Response>
rescue Late::ApiError => e
  puts "Error when calling CommentAutomationsApi->update_comment_automation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **automation_id** | **String** |  |  |
| **update_comment_automation_request** | [**UpdateCommentAutomationRequest**](UpdateCommentAutomationRequest.md) |  | [optional] |

### Return type

[**UpdateCommentAutomation200Response**](UpdateCommentAutomation200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

