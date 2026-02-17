# Late::AccountsApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**delete_account**](AccountsApi.md#delete_account) | **DELETE** /v1/accounts/{accountId} | Disconnect account |
| [**get_account_health**](AccountsApi.md#get_account_health) | **GET** /v1/accounts/{accountId}/health | Check account health |
| [**get_all_accounts_health**](AccountsApi.md#get_all_accounts_health) | **GET** /v1/accounts/health | Check accounts health |
| [**get_follower_stats**](AccountsApi.md#get_follower_stats) | **GET** /v1/accounts/follower-stats | Get follower stats |
| [**list_accounts**](AccountsApi.md#list_accounts) | **GET** /v1/accounts | List accounts |
| [**update_account**](AccountsApi.md#update_account) | **PUT** /v1/accounts/{accountId} | Update account |


## delete_account

> <DeleteAccountGroup200Response> delete_account(account_id)

Disconnect account

Disconnects and removes a connected social account.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::AccountsApi.new
account_id = 'account_id_example' # String | 

begin
  # Disconnect account
  result = api_instance.delete_account(account_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling AccountsApi->delete_account: #{e}"
end
```

#### Using the delete_account_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeleteAccountGroup200Response>, Integer, Hash)> delete_account_with_http_info(account_id)

```ruby
begin
  # Disconnect account
  data, status_code, headers = api_instance.delete_account_with_http_info(account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeleteAccountGroup200Response>
rescue Late::ApiError => e
  puts "Error when calling AccountsApi->delete_account_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |

### Return type

[**DeleteAccountGroup200Response**](DeleteAccountGroup200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_account_health

> <GetAccountHealth200Response> get_account_health(account_id)

Check account health

Returns detailed health info for a specific account including token status, permissions, and recommendations.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::AccountsApi.new
account_id = 'account_id_example' # String | The account ID to check

begin
  # Check account health
  result = api_instance.get_account_health(account_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling AccountsApi->get_account_health: #{e}"
end
```

#### Using the get_account_health_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetAccountHealth200Response>, Integer, Hash)> get_account_health_with_http_info(account_id)

```ruby
begin
  # Check account health
  data, status_code, headers = api_instance.get_account_health_with_http_info(account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetAccountHealth200Response>
rescue Late::ApiError => e
  puts "Error when calling AccountsApi->get_account_health_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** | The account ID to check |  |

### Return type

[**GetAccountHealth200Response**](GetAccountHealth200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_all_accounts_health

> <GetAllAccountsHealth200Response> get_all_accounts_health(opts)

Check accounts health

Returns health status of all connected accounts including token validity, permissions, and issues needing attention.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::AccountsApi.new
opts = {
  profile_id: 'profile_id_example', # String | Filter by profile ID
  platform: 'facebook', # String | Filter by platform
  status: 'healthy' # String | Filter by health status
}

begin
  # Check accounts health
  result = api_instance.get_all_accounts_health(opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling AccountsApi->get_all_accounts_health: #{e}"
end
```

#### Using the get_all_accounts_health_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetAllAccountsHealth200Response>, Integer, Hash)> get_all_accounts_health_with_http_info(opts)

```ruby
begin
  # Check accounts health
  data, status_code, headers = api_instance.get_all_accounts_health_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetAllAccountsHealth200Response>
rescue Late::ApiError => e
  puts "Error when calling AccountsApi->get_all_accounts_health_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** | Filter by profile ID | [optional] |
| **platform** | **String** | Filter by platform | [optional] |
| **status** | **String** | Filter by health status | [optional] |

### Return type

[**GetAllAccountsHealth200Response**](GetAllAccountsHealth200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_follower_stats

> <GetFollowerStats200Response> get_follower_stats(opts)

Get follower stats

Returns follower count history and growth metrics for connected social accounts. Requires analytics add-on subscription. Follower counts are refreshed once per day. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::AccountsApi.new
opts = {
  account_ids: 'account_ids_example', # String | Comma-separated list of account IDs (optional, defaults to all user's accounts)
  profile_id: 'profile_id_example', # String | Filter by profile ID
  from_date: Date.parse('2013-10-20'), # Date | Start date in YYYY-MM-DD format (defaults to 30 days ago)
  to_date: Date.parse('2013-10-20'), # Date | End date in YYYY-MM-DD format (defaults to today)
  granularity: 'daily' # String | Data aggregation level
}

begin
  # Get follower stats
  result = api_instance.get_follower_stats(opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling AccountsApi->get_follower_stats: #{e}"
end
```

#### Using the get_follower_stats_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetFollowerStats200Response>, Integer, Hash)> get_follower_stats_with_http_info(opts)

```ruby
begin
  # Get follower stats
  data, status_code, headers = api_instance.get_follower_stats_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetFollowerStats200Response>
rescue Late::ApiError => e
  puts "Error when calling AccountsApi->get_follower_stats_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_ids** | **String** | Comma-separated list of account IDs (optional, defaults to all user&#39;s accounts) | [optional] |
| **profile_id** | **String** | Filter by profile ID | [optional] |
| **from_date** | **Date** | Start date in YYYY-MM-DD format (defaults to 30 days ago) | [optional] |
| **to_date** | **Date** | End date in YYYY-MM-DD format (defaults to today) | [optional] |
| **granularity** | **String** | Data aggregation level | [optional][default to &#39;daily&#39;] |

### Return type

[**GetFollowerStats200Response**](GetFollowerStats200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_accounts

> <ListAccounts200Response> list_accounts(opts)

List accounts

Returns connected social accounts. Only includes accounts within the plan limit by default. Follower data requires analytics add-on.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::AccountsApi.new
opts = {
  profile_id: 'profile_id_example', # String | Filter accounts by profile ID
  include_over_limit: true # Boolean | When true, includes accounts from over-limit profiles.
}

begin
  # List accounts
  result = api_instance.list_accounts(opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling AccountsApi->list_accounts: #{e}"
end
```

#### Using the list_accounts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListAccounts200Response>, Integer, Hash)> list_accounts_with_http_info(opts)

```ruby
begin
  # List accounts
  data, status_code, headers = api_instance.list_accounts_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListAccounts200Response>
rescue Late::ApiError => e
  puts "Error when calling AccountsApi->list_accounts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** | Filter accounts by profile ID | [optional] |
| **include_over_limit** | **Boolean** | When true, includes accounts from over-limit profiles. | [optional][default to false] |

### Return type

[**ListAccounts200Response**](ListAccounts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_account

> <UpdateAccount200Response> update_account(account_id, update_account_request)

Update account

Updates a connected social account's display name or username override.

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::AccountsApi.new
account_id = 'account_id_example' # String | 
update_account_request = Late::UpdateAccountRequest.new # UpdateAccountRequest | 

begin
  # Update account
  result = api_instance.update_account(account_id, update_account_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling AccountsApi->update_account: #{e}"
end
```

#### Using the update_account_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UpdateAccount200Response>, Integer, Hash)> update_account_with_http_info(account_id, update_account_request)

```ruby
begin
  # Update account
  data, status_code, headers = api_instance.update_account_with_http_info(account_id, update_account_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UpdateAccount200Response>
rescue Late::ApiError => e
  puts "Error when calling AccountsApi->update_account_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |
| **update_account_request** | [**UpdateAccountRequest**](UpdateAccountRequest.md) |  |  |

### Return type

[**UpdateAccount200Response**](UpdateAccount200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

