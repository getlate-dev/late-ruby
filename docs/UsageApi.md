# Late::UsageApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_usage_stats**](UsageApi.md#get_usage_stats) | **GET** /v1/usage-stats | Get plan and usage stats for current account |


## get_usage_stats

> <UsageStats> get_usage_stats

Get plan and usage stats for current account

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::UsageApi.new

begin
  # Get plan and usage stats for current account
  result = api_instance.get_usage_stats
  p result
rescue Late::ApiError => e
  puts "Error when calling UsageApi->get_usage_stats: #{e}"
end
```

#### Using the get_usage_stats_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UsageStats>, Integer, Hash)> get_usage_stats_with_http_info

```ruby
begin
  # Get plan and usage stats for current account
  data, status_code, headers = api_instance.get_usage_stats_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UsageStats>
rescue Late::ApiError => e
  puts "Error when calling UsageApi->get_usage_stats_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**UsageStats**](UsageStats.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

