# Late::MessagesApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_inbox_conversation**](MessagesApi.md#get_inbox_conversation) | **GET** /v1/inbox/conversations/{conversationId} | Get conversation details |
| [**get_inbox_conversation_messages**](MessagesApi.md#get_inbox_conversation_messages) | **GET** /v1/inbox/conversations/{conversationId}/messages | Get messages in a conversation |
| [**list_inbox_conversations**](MessagesApi.md#list_inbox_conversations) | **GET** /v1/inbox/conversations | List conversations across all accounts |
| [**send_inbox_message**](MessagesApi.md#send_inbox_message) | **POST** /v1/inbox/conversations/{conversationId}/messages | Send a message |
| [**update_inbox_conversation**](MessagesApi.md#update_inbox_conversation) | **PUT** /v1/inbox/conversations/{conversationId} | Update conversation status |


## get_inbox_conversation

> <GetInboxConversation200Response> get_inbox_conversation(conversation_id, account_id)

Get conversation details

Retrieve details and metadata for a specific conversation. Requires accountId query parameter.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::MessagesApi.new
conversation_id = 'conversation_id_example' # String | The conversation ID (id field from list conversations endpoint). This is the platform-specific conversation identifier, not an internal database ID.
account_id = 'account_id_example' # String | The social account ID

begin
  # Get conversation details
  result = api_instance.get_inbox_conversation(conversation_id, account_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling MessagesApi->get_inbox_conversation: #{e}"
end
```

#### Using the get_inbox_conversation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetInboxConversation200Response>, Integer, Hash)> get_inbox_conversation_with_http_info(conversation_id, account_id)

```ruby
begin
  # Get conversation details
  data, status_code, headers = api_instance.get_inbox_conversation_with_http_info(conversation_id, account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetInboxConversation200Response>
rescue Late::ApiError => e
  puts "Error when calling MessagesApi->get_inbox_conversation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **conversation_id** | **String** | The conversation ID (id field from list conversations endpoint). This is the platform-specific conversation identifier, not an internal database ID. |  |
| **account_id** | **String** | The social account ID |  |

### Return type

[**GetInboxConversation200Response**](GetInboxConversation200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_inbox_conversation_messages

> <GetInboxConversationMessages200Response> get_inbox_conversation_messages(conversation_id, account_id)

Get messages in a conversation

Fetch messages for a specific conversation. Requires accountId query parameter.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::MessagesApi.new
conversation_id = 'conversation_id_example' # String | The conversation ID (id field from list conversations endpoint). This is the platform-specific conversation identifier, not an internal database ID.
account_id = 'account_id_example' # String | Social account ID

begin
  # Get messages in a conversation
  result = api_instance.get_inbox_conversation_messages(conversation_id, account_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling MessagesApi->get_inbox_conversation_messages: #{e}"
end
```

#### Using the get_inbox_conversation_messages_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetInboxConversationMessages200Response>, Integer, Hash)> get_inbox_conversation_messages_with_http_info(conversation_id, account_id)

```ruby
begin
  # Get messages in a conversation
  data, status_code, headers = api_instance.get_inbox_conversation_messages_with_http_info(conversation_id, account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetInboxConversationMessages200Response>
rescue Late::ApiError => e
  puts "Error when calling MessagesApi->get_inbox_conversation_messages_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **conversation_id** | **String** | The conversation ID (id field from list conversations endpoint). This is the platform-specific conversation identifier, not an internal database ID. |  |
| **account_id** | **String** | Social account ID |  |

### Return type

[**GetInboxConversationMessages200Response**](GetInboxConversationMessages200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_inbox_conversations

> <ListInboxConversations200Response> list_inbox_conversations(opts)

List conversations across all accounts

Fetch conversations (DMs) from all connected messaging accounts in a single API call. Supports filtering by profile and platform. Results are aggregated and deduplicated.  **Supported platforms:** Facebook, Instagram, Bluesky, Reddit, Telegram 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::MessagesApi.new
opts = {
  profile_id: 'profile_id_example', # String | Filter by profile ID
  platform: 'facebook', # String | Filter by platform
  status: 'active', # String | Filter by conversation status
  sort_order: 'asc', # String | Sort order by updated time
  limit: 56, # Integer | Maximum number of conversations to return
  cursor: 'cursor_example', # String | Pagination cursor for next page
  account_id: 'account_id_example' # String | Filter by specific social account ID
}

begin
  # List conversations across all accounts
  result = api_instance.list_inbox_conversations(opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling MessagesApi->list_inbox_conversations: #{e}"
end
```

#### Using the list_inbox_conversations_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListInboxConversations200Response>, Integer, Hash)> list_inbox_conversations_with_http_info(opts)

```ruby
begin
  # List conversations across all accounts
  data, status_code, headers = api_instance.list_inbox_conversations_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListInboxConversations200Response>
rescue Late::ApiError => e
  puts "Error when calling MessagesApi->list_inbox_conversations_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** | Filter by profile ID | [optional] |
| **platform** | **String** | Filter by platform | [optional] |
| **status** | **String** | Filter by conversation status | [optional] |
| **sort_order** | **String** | Sort order by updated time | [optional][default to &#39;desc&#39;] |
| **limit** | **Integer** | Maximum number of conversations to return | [optional][default to 50] |
| **cursor** | **String** | Pagination cursor for next page | [optional] |
| **account_id** | **String** | Filter by specific social account ID | [optional] |

### Return type

[**ListInboxConversations200Response**](ListInboxConversations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## send_inbox_message

> <SendInboxMessage200Response> send_inbox_message(conversation_id, send_inbox_message_request)

Send a message

Send a message in a conversation. Requires accountId in request body.  **Attachment support by platform:** - Telegram: Images, videos, documents (up to 50MB) - Facebook Messenger: Images, videos, audio, files - Twitter/X: Images, videos (requires media upload) - Instagram: Not supported (API limitation) - Bluesky: Not supported (API limitation) - Reddit: Not supported (API limitation) 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::MessagesApi.new
conversation_id = 'conversation_id_example' # String | The conversation ID (id field from list conversations endpoint). This is the platform-specific conversation identifier, not an internal database ID.
send_inbox_message_request = Late::SendInboxMessageRequest.new({account_id: 'account_id_example', message: 'message_example'}) # SendInboxMessageRequest | 

begin
  # Send a message
  result = api_instance.send_inbox_message(conversation_id, send_inbox_message_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling MessagesApi->send_inbox_message: #{e}"
end
```

#### Using the send_inbox_message_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SendInboxMessage200Response>, Integer, Hash)> send_inbox_message_with_http_info(conversation_id, send_inbox_message_request)

```ruby
begin
  # Send a message
  data, status_code, headers = api_instance.send_inbox_message_with_http_info(conversation_id, send_inbox_message_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SendInboxMessage200Response>
rescue Late::ApiError => e
  puts "Error when calling MessagesApi->send_inbox_message_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **conversation_id** | **String** | The conversation ID (id field from list conversations endpoint). This is the platform-specific conversation identifier, not an internal database ID. |  |
| **send_inbox_message_request** | [**SendInboxMessageRequest**](SendInboxMessageRequest.md) |  |  |

### Return type

[**SendInboxMessage200Response**](SendInboxMessage200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json, multipart/form-data
- **Accept**: application/json


## update_inbox_conversation

> <UpdateInboxConversation200Response> update_inbox_conversation(conversation_id, update_inbox_conversation_request)

Update conversation status

Archive or activate a conversation. Requires accountId in request body.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::MessagesApi.new
conversation_id = 'conversation_id_example' # String | The conversation ID (id field from list conversations endpoint). This is the platform-specific conversation identifier, not an internal database ID.
update_inbox_conversation_request = Late::UpdateInboxConversationRequest.new({account_id: 'account_id_example', status: 'active'}) # UpdateInboxConversationRequest | 

begin
  # Update conversation status
  result = api_instance.update_inbox_conversation(conversation_id, update_inbox_conversation_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling MessagesApi->update_inbox_conversation: #{e}"
end
```

#### Using the update_inbox_conversation_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UpdateInboxConversation200Response>, Integer, Hash)> update_inbox_conversation_with_http_info(conversation_id, update_inbox_conversation_request)

```ruby
begin
  # Update conversation status
  data, status_code, headers = api_instance.update_inbox_conversation_with_http_info(conversation_id, update_inbox_conversation_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UpdateInboxConversation200Response>
rescue Late::ApiError => e
  puts "Error when calling MessagesApi->update_inbox_conversation_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **conversation_id** | **String** | The conversation ID (id field from list conversations endpoint). This is the platform-specific conversation identifier, not an internal database ID. |  |
| **update_inbox_conversation_request** | [**UpdateInboxConversationRequest**](UpdateInboxConversationRequest.md) |  |  |

### Return type

[**UpdateInboxConversation200Response**](UpdateInboxConversation200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

