# Late::GMBFoodMenusApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_google_business_food_menus**](GMBFoodMenusApi.md#get_google_business_food_menus) | **GET** /v1/accounts/{accountId}/gmb-food-menus | Get Google Business Profile food menus |
| [**update_google_business_food_menus**](GMBFoodMenusApi.md#update_google_business_food_menus) | **PUT** /v1/accounts/{accountId}/gmb-food-menus | Update Google Business Profile food menus |


## get_google_business_food_menus

> <GetGoogleBusinessFoodMenus200Response> get_google_business_food_menus(account_id)

Get Google Business Profile food menus

Fetches food menus for a connected Google Business Profile location.  Returns the full menu structure including: - Menu names and descriptions - Sections (e.g. Appetizers, Entrees, Drinks) - Items with labels, pricing, dietary info, and allergens - Item options/variants  Only available for locations with food menu support (restaurants, cafes, etc.). 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::GMBFoodMenusApi.new
account_id = 'account_id_example' # String | The Late account ID (from /v1/accounts)

begin
  # Get Google Business Profile food menus
  result = api_instance.get_google_business_food_menus(account_id)
  p result
rescue Late::ApiError => e
  puts "Error when calling GMBFoodMenusApi->get_google_business_food_menus: #{e}"
end
```

#### Using the get_google_business_food_menus_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetGoogleBusinessFoodMenus200Response>, Integer, Hash)> get_google_business_food_menus_with_http_info(account_id)

```ruby
begin
  # Get Google Business Profile food menus
  data, status_code, headers = api_instance.get_google_business_food_menus_with_http_info(account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetGoogleBusinessFoodMenus200Response>
rescue Late::ApiError => e
  puts "Error when calling GMBFoodMenusApi->get_google_business_food_menus_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** | The Late account ID (from /v1/accounts) |  |

### Return type

[**GetGoogleBusinessFoodMenus200Response**](GetGoogleBusinessFoodMenus200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_google_business_food_menus

> <UpdateGoogleBusinessFoodMenus200Response> update_google_business_food_menus(account_id, update_google_business_food_menus_request)

Update Google Business Profile food menus

Updates the food menus for a connected Google Business Profile location.  Send the full menus array. Use `updateMask` for partial updates (e.g. `\"menus\"` to only update the menus field).  Each menu can contain sections, and each section can contain items with pricing, dietary restrictions, allergens, and more. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::GMBFoodMenusApi.new
account_id = 'account_id_example' # String | The Late account ID (from /v1/accounts)
update_google_business_food_menus_request = Late::UpdateGoogleBusinessFoodMenusRequest.new({menus: [Late::FoodMenu.new({labels: [Late::FoodMenuLabel.new({display_name: 'display_name_example'})]})]}) # UpdateGoogleBusinessFoodMenusRequest | 

begin
  # Update Google Business Profile food menus
  result = api_instance.update_google_business_food_menus(account_id, update_google_business_food_menus_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling GMBFoodMenusApi->update_google_business_food_menus: #{e}"
end
```

#### Using the update_google_business_food_menus_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UpdateGoogleBusinessFoodMenus200Response>, Integer, Hash)> update_google_business_food_menus_with_http_info(account_id, update_google_business_food_menus_request)

```ruby
begin
  # Update Google Business Profile food menus
  data, status_code, headers = api_instance.update_google_business_food_menus_with_http_info(account_id, update_google_business_food_menus_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UpdateGoogleBusinessFoodMenus200Response>
rescue Late::ApiError => e
  puts "Error when calling GMBFoodMenusApi->update_google_business_food_menus_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** | The Late account ID (from /v1/accounts) |  |
| **update_google_business_food_menus_request** | [**UpdateGoogleBusinessFoodMenusRequest**](UpdateGoogleBusinessFoodMenusRequest.md) |  |  |

### Return type

[**UpdateGoogleBusinessFoodMenus200Response**](UpdateGoogleBusinessFoodMenus200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

