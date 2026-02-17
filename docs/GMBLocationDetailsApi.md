# Late::GMBLocationDetailsApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_google_business_location_details**](GMBLocationDetailsApi.md#get_google_business_location_details) | **GET** /v1/accounts/{accountId}/gmb-location-details | Get location details |
| [**update_google_business_location_details**](GMBLocationDetailsApi.md#update_google_business_location_details) | **PUT** /v1/accounts/{accountId}/gmb-location-details | Update location details |


## get_google_business_location_details

> <GetGoogleBusinessLocationDetails200Response> get_google_business_location_details(account_id, opts)

Get location details

Fetches detailed location information including opening hours, special hours, business description, phone numbers, website, categories, and more.  Use the readMask query parameter to request specific fields. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::GMBLocationDetailsApi.new
account_id = 'account_id_example' # String | The Late account ID (from /v1/accounts)
opts = {
  read_mask: 'read_mask_example' # String | Comma-separated fields to return. Defaults to common fields. Available: name, title, phoneNumbers, categories, storefrontAddress, websiteUri, regularHours, specialHours, serviceArea, profile, openInfo, metadata, moreHours 
}

begin
  # Get location details
  result = api_instance.get_google_business_location_details(account_id, opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling GMBLocationDetailsApi->get_google_business_location_details: #{e}"
end
```

#### Using the get_google_business_location_details_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetGoogleBusinessLocationDetails200Response>, Integer, Hash)> get_google_business_location_details_with_http_info(account_id, opts)

```ruby
begin
  # Get location details
  data, status_code, headers = api_instance.get_google_business_location_details_with_http_info(account_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetGoogleBusinessLocationDetails200Response>
rescue Late::ApiError => e
  puts "Error when calling GMBLocationDetailsApi->get_google_business_location_details_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** | The Late account ID (from /v1/accounts) |  |
| **read_mask** | **String** | Comma-separated fields to return. Defaults to common fields. Available: name, title, phoneNumbers, categories, storefrontAddress, websiteUri, regularHours, specialHours, serviceArea, profile, openInfo, metadata, moreHours  | [optional] |

### Return type

[**GetGoogleBusinessLocationDetails200Response**](GetGoogleBusinessLocationDetails200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_google_business_location_details

> <UpdateGoogleBusinessLocationDetails200Response> update_google_business_location_details(account_id, update_google_business_location_details_request)

Update location details

Updates location details such as opening hours, special hours, business description, phone, and website. The updateMask field is required and specifies which fields to update. Common masks: regularHours, specialHours, profile.description, websiteUri, phoneNumbers. Combine with commas (e.g. regularHours,specialHours). 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::GMBLocationDetailsApi.new
account_id = 'account_id_example' # String | The Late account ID (from /v1/accounts)
update_google_business_location_details_request = Late::UpdateGoogleBusinessLocationDetailsRequest.new({update_mask: 'update_mask_example'}) # UpdateGoogleBusinessLocationDetailsRequest | 

begin
  # Update location details
  result = api_instance.update_google_business_location_details(account_id, update_google_business_location_details_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling GMBLocationDetailsApi->update_google_business_location_details: #{e}"
end
```

#### Using the update_google_business_location_details_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UpdateGoogleBusinessLocationDetails200Response>, Integer, Hash)> update_google_business_location_details_with_http_info(account_id, update_google_business_location_details_request)

```ruby
begin
  # Update location details
  data, status_code, headers = api_instance.update_google_business_location_details_with_http_info(account_id, update_google_business_location_details_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UpdateGoogleBusinessLocationDetails200Response>
rescue Late::ApiError => e
  puts "Error when calling GMBLocationDetailsApi->update_google_business_location_details_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** | The Late account ID (from /v1/accounts) |  |
| **update_google_business_location_details_request** | [**UpdateGoogleBusinessLocationDetailsRequest**](UpdateGoogleBusinessLocationDetailsRequest.md) |  |  |

### Return type

[**UpdateGoogleBusinessLocationDetails200Response**](UpdateGoogleBusinessLocationDetails200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

