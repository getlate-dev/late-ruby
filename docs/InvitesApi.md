# Late::InvitesApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_invite_token**](InvitesApi.md#create_invite_token) | **POST** /v1/invite/tokens | Create invite token |


## create_invite_token

> <CreateInviteToken201Response> create_invite_token(create_invite_token_request)

Create invite token

Generate a secure invite link to grant team members access to your profiles. Invites expire after 7 days and are single-use. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::InvitesApi.new
create_invite_token_request = Late::CreateInviteTokenRequest.new({scope: 'all'}) # CreateInviteTokenRequest | 

begin
  # Create invite token
  result = api_instance.create_invite_token(create_invite_token_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling InvitesApi->create_invite_token: #{e}"
end
```

#### Using the create_invite_token_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateInviteToken201Response>, Integer, Hash)> create_invite_token_with_http_info(create_invite_token_request)

```ruby
begin
  # Create invite token
  data, status_code, headers = api_instance.create_invite_token_with_http_info(create_invite_token_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateInviteToken201Response>
rescue Late::ApiError => e
  puts "Error when calling InvitesApi->create_invite_token_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_invite_token_request** | [**CreateInviteTokenRequest**](CreateInviteTokenRequest.md) |  |  |

### Return type

[**CreateInviteToken201Response**](CreateInviteToken201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

