# Late::WebhooksApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_webhook_settings**](WebhooksApi.md#create_webhook_settings) | **POST** /v1/webhooks/settings | Create a new webhook |
| [**delete_webhook_settings**](WebhooksApi.md#delete_webhook_settings) | **DELETE** /v1/webhooks/settings | Delete a webhook |
| [**get_webhook_logs**](WebhooksApi.md#get_webhook_logs) | **GET** /v1/webhooks/logs | Get webhook delivery logs |
| [**get_webhook_settings**](WebhooksApi.md#get_webhook_settings) | **GET** /v1/webhooks/settings | List all webhooks |
| [**test_webhook**](WebhooksApi.md#test_webhook) | **POST** /v1/webhooks/test | Send test webhook |
| [**update_webhook_settings**](WebhooksApi.md#update_webhook_settings) | **PUT** /v1/webhooks/settings | Update a webhook |


## create_webhook_settings

> <UpdateWebhookSettings200Response> create_webhook_settings(create_webhook_settings_request)

Create a new webhook

Create a new webhook configuration. Maximum 10 webhooks per user.  **Note:** Webhooks are automatically disabled after 10 consecutive delivery failures. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WebhooksApi.new
create_webhook_settings_request = Late::CreateWebhookSettingsRequest.new # CreateWebhookSettingsRequest | 

begin
  # Create a new webhook
  result = api_instance.create_webhook_settings(create_webhook_settings_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling WebhooksApi->create_webhook_settings: #{e}"
end
```

#### Using the create_webhook_settings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UpdateWebhookSettings200Response>, Integer, Hash)> create_webhook_settings_with_http_info(create_webhook_settings_request)

```ruby
begin
  # Create a new webhook
  data, status_code, headers = api_instance.create_webhook_settings_with_http_info(create_webhook_settings_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UpdateWebhookSettings200Response>
rescue Late::ApiError => e
  puts "Error when calling WebhooksApi->create_webhook_settings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_webhook_settings_request** | [**CreateWebhookSettingsRequest**](CreateWebhookSettingsRequest.md) |  |  |

### Return type

[**UpdateWebhookSettings200Response**](UpdateWebhookSettings200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_webhook_settings

> <UpdateRedditSubreddits200Response> delete_webhook_settings(id)

Delete a webhook

Permanently delete a webhook configuration.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WebhooksApi.new
id = 'id_example' # String | Webhook ID to delete

begin
  # Delete a webhook
  result = api_instance.delete_webhook_settings(id)
  p result
rescue Late::ApiError => e
  puts "Error when calling WebhooksApi->delete_webhook_settings: #{e}"
end
```

#### Using the delete_webhook_settings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UpdateRedditSubreddits200Response>, Integer, Hash)> delete_webhook_settings_with_http_info(id)

```ruby
begin
  # Delete a webhook
  data, status_code, headers = api_instance.delete_webhook_settings_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UpdateRedditSubreddits200Response>
rescue Late::ApiError => e
  puts "Error when calling WebhooksApi->delete_webhook_settings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Webhook ID to delete |  |

### Return type

[**UpdateRedditSubreddits200Response**](UpdateRedditSubreddits200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_webhook_logs

> <GetWebhookLogs200Response> get_webhook_logs(opts)

Get webhook delivery logs

Retrieve webhook delivery history. Logs are automatically deleted after 7 days. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WebhooksApi.new
opts = {
  limit: 56, # Integer | Maximum number of logs to return (max 100)
  status: 'success', # String | Filter by delivery status
  event: 'post.scheduled', # String | Filter by event type
  webhook_id: 'webhook_id_example' # String | Filter by webhook ID
}

begin
  # Get webhook delivery logs
  result = api_instance.get_webhook_logs(opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling WebhooksApi->get_webhook_logs: #{e}"
end
```

#### Using the get_webhook_logs_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetWebhookLogs200Response>, Integer, Hash)> get_webhook_logs_with_http_info(opts)

```ruby
begin
  # Get webhook delivery logs
  data, status_code, headers = api_instance.get_webhook_logs_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetWebhookLogs200Response>
rescue Late::ApiError => e
  puts "Error when calling WebhooksApi->get_webhook_logs_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **limit** | **Integer** | Maximum number of logs to return (max 100) | [optional][default to 50] |
| **status** | **String** | Filter by delivery status | [optional] |
| **event** | **String** | Filter by event type | [optional] |
| **webhook_id** | **String** | Filter by webhook ID | [optional] |

### Return type

[**GetWebhookLogs200Response**](GetWebhookLogs200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_webhook_settings

> <GetWebhookSettings200Response> get_webhook_settings

List all webhooks

Retrieve all configured webhooks for the authenticated user. Supports up to 10 webhooks per user.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WebhooksApi.new

begin
  # List all webhooks
  result = api_instance.get_webhook_settings
  p result
rescue Late::ApiError => e
  puts "Error when calling WebhooksApi->get_webhook_settings: #{e}"
end
```

#### Using the get_webhook_settings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetWebhookSettings200Response>, Integer, Hash)> get_webhook_settings_with_http_info

```ruby
begin
  # List all webhooks
  data, status_code, headers = api_instance.get_webhook_settings_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetWebhookSettings200Response>
rescue Late::ApiError => e
  puts "Error when calling WebhooksApi->get_webhook_settings_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**GetWebhookSettings200Response**](GetWebhookSettings200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## test_webhook

> <UnpublishPost200Response> test_webhook(test_webhook_request)

Send test webhook

Send a test webhook to verify your endpoint is configured correctly. The test payload includes `event: \"webhook.test\"` to distinguish it from real events. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WebhooksApi.new
test_webhook_request = Late::TestWebhookRequest.new({webhook_id: 'webhook_id_example'}) # TestWebhookRequest | 

begin
  # Send test webhook
  result = api_instance.test_webhook(test_webhook_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling WebhooksApi->test_webhook: #{e}"
end
```

#### Using the test_webhook_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UnpublishPost200Response>, Integer, Hash)> test_webhook_with_http_info(test_webhook_request)

```ruby
begin
  # Send test webhook
  data, status_code, headers = api_instance.test_webhook_with_http_info(test_webhook_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UnpublishPost200Response>
rescue Late::ApiError => e
  puts "Error when calling WebhooksApi->test_webhook_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **test_webhook_request** | [**TestWebhookRequest**](TestWebhookRequest.md) |  |  |

### Return type

[**UnpublishPost200Response**](UnpublishPost200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_webhook_settings

> <UpdateWebhookSettings200Response> update_webhook_settings(update_webhook_settings_request)

Update a webhook

Update an existing webhook configuration. All fields except `_id` are optional - only provided fields will be updated.  **Note:** Webhooks are automatically disabled after 10 consecutive delivery failures. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::WebhooksApi.new
update_webhook_settings_request = Late::UpdateWebhookSettingsRequest.new({_id: '_id_example'}) # UpdateWebhookSettingsRequest | 

begin
  # Update a webhook
  result = api_instance.update_webhook_settings(update_webhook_settings_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling WebhooksApi->update_webhook_settings: #{e}"
end
```

#### Using the update_webhook_settings_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UpdateWebhookSettings200Response>, Integer, Hash)> update_webhook_settings_with_http_info(update_webhook_settings_request)

```ruby
begin
  # Update a webhook
  data, status_code, headers = api_instance.update_webhook_settings_with_http_info(update_webhook_settings_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UpdateWebhookSettings200Response>
rescue Late::ApiError => e
  puts "Error when calling WebhooksApi->update_webhook_settings_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **update_webhook_settings_request** | [**UpdateWebhookSettingsRequest**](UpdateWebhookSettingsRequest.md) |  |  |

### Return type

[**UpdateWebhookSettings200Response**](UpdateWebhookSettings200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

