# Late::AccountSettingsApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**delete_instagram_ice_breakers**](AccountSettingsApi.md#delete_instagram_ice_breakers) | **DELETE** /v1/accounts/{accountId}/instagram-ice-breakers | Delete Instagram ice breakers |
| [**delete_messenger_menu**](AccountSettingsApi.md#delete_messenger_menu) | **DELETE** /v1/accounts/{accountId}/messenger-menu | Delete Facebook persistent menu |
| [**delete_telegram_commands**](AccountSettingsApi.md#delete_telegram_commands) | **DELETE** /v1/accounts/{accountId}/telegram-commands | Delete Telegram bot commands |
| [**get_instagram_ice_breakers**](AccountSettingsApi.md#get_instagram_ice_breakers) | **GET** /v1/accounts/{accountId}/instagram-ice-breakers | Get Instagram ice breakers |
| [**get_messenger_menu**](AccountSettingsApi.md#get_messenger_menu) | **GET** /v1/accounts/{accountId}/messenger-menu | Get Facebook persistent menu |
| [**get_telegram_commands**](AccountSettingsApi.md#get_telegram_commands) | **GET** /v1/accounts/{accountId}/telegram-commands | Get Telegram bot commands |
| [**set_instagram_ice_breakers**](AccountSettingsApi.md#set_instagram_ice_breakers) | **PUT** /v1/accounts/{accountId}/instagram-ice-breakers | Set Instagram ice breakers |
| [**set_messenger_menu**](AccountSettingsApi.md#set_messenger_menu) | **PUT** /v1/accounts/{accountId}/messenger-menu | Set Facebook persistent menu |
| [**set_telegram_commands**](AccountSettingsApi.md#set_telegram_commands) | **PUT** /v1/accounts/{accountId}/telegram-commands | Set Telegram bot commands |


## delete_instagram_ice_breakers

> delete_instagram_ice_breakers(account_id)

Delete Instagram ice breakers

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::AccountSettingsApi.new
account_id = 'account_id_example' # String | 

begin
  # Delete Instagram ice breakers
  api_instance.delete_instagram_ice_breakers(account_id)
rescue Late::ApiError => e
  puts "Error when calling AccountSettingsApi->delete_instagram_ice_breakers: #{e}"
end
```

#### Using the delete_instagram_ice_breakers_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_instagram_ice_breakers_with_http_info(account_id)

```ruby
begin
  # Delete Instagram ice breakers
  data, status_code, headers = api_instance.delete_instagram_ice_breakers_with_http_info(account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Late::ApiError => e
  puts "Error when calling AccountSettingsApi->delete_instagram_ice_breakers_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## delete_messenger_menu

> delete_messenger_menu(account_id)

Delete Facebook persistent menu

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::AccountSettingsApi.new
account_id = 'account_id_example' # String | 

begin
  # Delete Facebook persistent menu
  api_instance.delete_messenger_menu(account_id)
rescue Late::ApiError => e
  puts "Error when calling AccountSettingsApi->delete_messenger_menu: #{e}"
end
```

#### Using the delete_messenger_menu_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_messenger_menu_with_http_info(account_id)

```ruby
begin
  # Delete Facebook persistent menu
  data, status_code, headers = api_instance.delete_messenger_menu_with_http_info(account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Late::ApiError => e
  puts "Error when calling AccountSettingsApi->delete_messenger_menu_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## delete_telegram_commands

> delete_telegram_commands(account_id)

Delete Telegram bot commands

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::AccountSettingsApi.new
account_id = 'account_id_example' # String | 

begin
  # Delete Telegram bot commands
  api_instance.delete_telegram_commands(account_id)
rescue Late::ApiError => e
  puts "Error when calling AccountSettingsApi->delete_telegram_commands: #{e}"
end
```

#### Using the delete_telegram_commands_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_telegram_commands_with_http_info(account_id)

```ruby
begin
  # Delete Telegram bot commands
  data, status_code, headers = api_instance.delete_telegram_commands_with_http_info(account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Late::ApiError => e
  puts "Error when calling AccountSettingsApi->delete_telegram_commands_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_instagram_ice_breakers

> <GetMessengerMenu200Response> get_instagram_ice_breakers(account_id)

Get Instagram ice breakers

Get the ice breaker configuration for an Instagram account.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::AccountSettingsApi.new
account_id = 'account_id_example' # String | 

begin
  # Get Instagram ice breakers
  result = api_instance.get_instagram_ice_breakers(account_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling AccountSettingsApi->get_instagram_ice_breakers: #{e}"
end
```

#### Using the get_instagram_ice_breakers_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetMessengerMenu200Response>, Integer, Hash)> get_instagram_ice_breakers_with_http_info(account_id)

```ruby
begin
  # Get Instagram ice breakers
  data, status_code, headers = api_instance.get_instagram_ice_breakers_with_http_info(account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetMessengerMenu200Response>
rescue Late::ApiError => e
  puts "Error when calling AccountSettingsApi->get_instagram_ice_breakers_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |

### Return type

[**GetMessengerMenu200Response**](GetMessengerMenu200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_messenger_menu

> <GetMessengerMenu200Response> get_messenger_menu(account_id)

Get Facebook persistent menu

Get the persistent menu configuration for a Facebook Messenger account.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::AccountSettingsApi.new
account_id = 'account_id_example' # String | 

begin
  # Get Facebook persistent menu
  result = api_instance.get_messenger_menu(account_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling AccountSettingsApi->get_messenger_menu: #{e}"
end
```

#### Using the get_messenger_menu_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetMessengerMenu200Response>, Integer, Hash)> get_messenger_menu_with_http_info(account_id)

```ruby
begin
  # Get Facebook persistent menu
  data, status_code, headers = api_instance.get_messenger_menu_with_http_info(account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetMessengerMenu200Response>
rescue Late::ApiError => e
  puts "Error when calling AccountSettingsApi->get_messenger_menu_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |

### Return type

[**GetMessengerMenu200Response**](GetMessengerMenu200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_telegram_commands

> <GetTelegramCommands200Response> get_telegram_commands(account_id)

Get Telegram bot commands

Get the bot commands configuration for a Telegram account.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::AccountSettingsApi.new
account_id = 'account_id_example' # String | 

begin
  # Get Telegram bot commands
  result = api_instance.get_telegram_commands(account_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling AccountSettingsApi->get_telegram_commands: #{e}"
end
```

#### Using the get_telegram_commands_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetTelegramCommands200Response>, Integer, Hash)> get_telegram_commands_with_http_info(account_id)

```ruby
begin
  # Get Telegram bot commands
  data, status_code, headers = api_instance.get_telegram_commands_with_http_info(account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetTelegramCommands200Response>
rescue Late::ApiError => e
  puts "Error when calling AccountSettingsApi->get_telegram_commands_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |

### Return type

[**GetTelegramCommands200Response**](GetTelegramCommands200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## set_instagram_ice_breakers

> set_instagram_ice_breakers(account_id, set_instagram_ice_breakers_request)

Set Instagram ice breakers

Set ice breakers for an Instagram account. Max 4 ice breakers, question max 80 chars.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::AccountSettingsApi.new
account_id = 'account_id_example' # String | 
set_instagram_ice_breakers_request = Late::SetInstagramIceBreakersRequest.new({ice_breakers: [Late::SetInstagramIceBreakersRequestIceBreakersInner.new({question: 'question_example', payload: 'payload_example'})]}) # SetInstagramIceBreakersRequest | 

begin
  # Set Instagram ice breakers
  api_instance.set_instagram_ice_breakers(account_id, set_instagram_ice_breakers_request)
rescue Late::ApiError => e
  puts "Error when calling AccountSettingsApi->set_instagram_ice_breakers: #{e}"
end
```

#### Using the set_instagram_ice_breakers_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> set_instagram_ice_breakers_with_http_info(account_id, set_instagram_ice_breakers_request)

```ruby
begin
  # Set Instagram ice breakers
  data, status_code, headers = api_instance.set_instagram_ice_breakers_with_http_info(account_id, set_instagram_ice_breakers_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Late::ApiError => e
  puts "Error when calling AccountSettingsApi->set_instagram_ice_breakers_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |
| **set_instagram_ice_breakers_request** | [**SetInstagramIceBreakersRequest**](SetInstagramIceBreakersRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## set_messenger_menu

> set_messenger_menu(account_id, set_messenger_menu_request)

Set Facebook persistent menu

Set the persistent menu for a Facebook Messenger account. Max 3 top-level items, max 5 nested items.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::AccountSettingsApi.new
account_id = 'account_id_example' # String | 
set_messenger_menu_request = Late::SetMessengerMenuRequest.new({persistent_menu: [3.56]}) # SetMessengerMenuRequest | 

begin
  # Set Facebook persistent menu
  api_instance.set_messenger_menu(account_id, set_messenger_menu_request)
rescue Late::ApiError => e
  puts "Error when calling AccountSettingsApi->set_messenger_menu: #{e}"
end
```

#### Using the set_messenger_menu_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> set_messenger_menu_with_http_info(account_id, set_messenger_menu_request)

```ruby
begin
  # Set Facebook persistent menu
  data, status_code, headers = api_instance.set_messenger_menu_with_http_info(account_id, set_messenger_menu_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Late::ApiError => e
  puts "Error when calling AccountSettingsApi->set_messenger_menu_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |
| **set_messenger_menu_request** | [**SetMessengerMenuRequest**](SetMessengerMenuRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## set_telegram_commands

> set_telegram_commands(account_id, set_telegram_commands_request)

Set Telegram bot commands

Set bot commands for a Telegram account.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::AccountSettingsApi.new
account_id = 'account_id_example' # String | 
set_telegram_commands_request = Late::SetTelegramCommandsRequest.new({commands: [Late::SetTelegramCommandsRequestCommandsInner.new({command: 'command_example', description: 'description_example'})]}) # SetTelegramCommandsRequest | 

begin
  # Set Telegram bot commands
  api_instance.set_telegram_commands(account_id, set_telegram_commands_request)
rescue Late::ApiError => e
  puts "Error when calling AccountSettingsApi->set_telegram_commands: #{e}"
end
```

#### Using the set_telegram_commands_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> set_telegram_commands_with_http_info(account_id, set_telegram_commands_request)

```ruby
begin
  # Set Telegram bot commands
  data, status_code, headers = api_instance.set_telegram_commands_with_http_info(account_id, set_telegram_commands_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Late::ApiError => e
  puts "Error when calling AccountSettingsApi->set_telegram_commands_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |
| **set_telegram_commands_request** | [**SetTelegramCommandsRequest**](SetTelegramCommandsRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

