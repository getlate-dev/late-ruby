# Late::GMBAttributesApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_google_business_attributes**](GMBAttributesApi.md#get_google_business_attributes) | **GET** /v1/accounts/{accountId}/gmb-attributes | Get attributes |
| [**update_google_business_attributes**](GMBAttributesApi.md#update_google_business_attributes) | **PUT** /v1/accounts/{accountId}/gmb-attributes | Update attributes |


## get_google_business_attributes

> <GetGoogleBusinessAttributes200Response> get_google_business_attributes(account_id)

Get attributes

Fetches location attributes such as amenities, services, and accessibility features.  Common attributes for restaurants include: - Dining options: has_dine_in, has_takeout, has_delivery - Amenities: has_outdoor_seating, has_wifi, has_parking - Accessibility: has_wheelchair_accessible_entrance - Payments: pay_credit_card_types_accepted  Available attributes vary by business category. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::GMBAttributesApi.new
account_id = 'account_id_example' # String | 

begin
  # Get attributes
  result = api_instance.get_google_business_attributes(account_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling GMBAttributesApi->get_google_business_attributes: #{e}"
end
```

#### Using the get_google_business_attributes_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetGoogleBusinessAttributes200Response>, Integer, Hash)> get_google_business_attributes_with_http_info(account_id)

```ruby
begin
  # Get attributes
  data, status_code, headers = api_instance.get_google_business_attributes_with_http_info(account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetGoogleBusinessAttributes200Response>
rescue Late::ApiError => e
  puts "Error when calling GMBAttributesApi->get_google_business_attributes_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |

### Return type

[**GetGoogleBusinessAttributes200Response**](GetGoogleBusinessAttributes200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_google_business_attributes

> <UpdateGoogleBusinessAttributes200Response> update_google_business_attributes(account_id, update_google_business_attributes_request)

Update attributes

Updates location attributes (amenities, services, etc.).  The `attributeMask` specifies which attributes to update (comma-separated). 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::GMBAttributesApi.new
account_id = 'account_id_example' # String | 
update_google_business_attributes_request = Late::UpdateGoogleBusinessAttributesRequest.new({attributes: [Late::UpdateGoogleBusinessAttributesRequestAttributesInner.new], attribute_mask: 'attribute_mask_example'}) # UpdateGoogleBusinessAttributesRequest | 

begin
  # Update attributes
  result = api_instance.update_google_business_attributes(account_id, update_google_business_attributes_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling GMBAttributesApi->update_google_business_attributes: #{e}"
end
```

#### Using the update_google_business_attributes_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UpdateGoogleBusinessAttributes200Response>, Integer, Hash)> update_google_business_attributes_with_http_info(account_id, update_google_business_attributes_request)

```ruby
begin
  # Update attributes
  data, status_code, headers = api_instance.update_google_business_attributes_with_http_info(account_id, update_google_business_attributes_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UpdateGoogleBusinessAttributes200Response>
rescue Late::ApiError => e
  puts "Error when calling GMBAttributesApi->update_google_business_attributes_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |
| **update_google_business_attributes_request** | [**UpdateGoogleBusinessAttributesRequest**](UpdateGoogleBusinessAttributesRequest.md) |  |  |

### Return type

[**UpdateGoogleBusinessAttributes200Response**](UpdateGoogleBusinessAttributes200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

