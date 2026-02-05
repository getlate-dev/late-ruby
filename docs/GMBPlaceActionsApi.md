# Late::GMBPlaceActionsApi

All URIs are relative to *https://getlate.dev/api*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_google_business_place_action**](GMBPlaceActionsApi.md#create_google_business_place_action) | **POST** /v1/accounts/{accountId}/gmb-place-actions | Create a place action link (booking, ordering, reservation) |
| [**delete_google_business_place_action**](GMBPlaceActionsApi.md#delete_google_business_place_action) | **DELETE** /v1/accounts/{accountId}/gmb-place-actions | Delete a place action link |
| [**list_google_business_place_actions**](GMBPlaceActionsApi.md#list_google_business_place_actions) | **GET** /v1/accounts/{accountId}/gmb-place-actions | List place action links (booking, ordering, reservations) |


## create_google_business_place_action

> <CreateGoogleBusinessPlaceAction200Response> create_google_business_place_action(account_id, create_google_business_place_action_request)

Create a place action link (booking, ordering, reservation)

Creates a place action link for a location.  Available action types: - `APPOINTMENT` - Booking an appointment - `ONLINE_APPOINTMENT` - Booking an online appointment - `DINING_RESERVATION` - Making a dining reservation (OpenTable, Resy, etc.) - `FOOD_ORDERING` - Ordering food for delivery and/or takeout (DoorDash, Uber Eats, etc.) - `FOOD_DELIVERY` - Ordering food for delivery only - `FOOD_TAKEOUT` - Ordering food for takeout only - `SHOP_ONLINE` - Shopping with delivery and/or pickup 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::GMBPlaceActionsApi.new
account_id = 'account_id_example' # String | 
create_google_business_place_action_request = Late::CreateGoogleBusinessPlaceActionRequest.new({uri: 'uri_example', place_action_type: 'APPOINTMENT'}) # CreateGoogleBusinessPlaceActionRequest | 

begin
  # Create a place action link (booking, ordering, reservation)
  result = api_instance.create_google_business_place_action(account_id, create_google_business_place_action_request)
  p result
rescue Late::ApiError => e
  puts "Error when calling GMBPlaceActionsApi->create_google_business_place_action: #{e}"
end
```

#### Using the create_google_business_place_action_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreateGoogleBusinessPlaceAction200Response>, Integer, Hash)> create_google_business_place_action_with_http_info(account_id, create_google_business_place_action_request)

```ruby
begin
  # Create a place action link (booking, ordering, reservation)
  data, status_code, headers = api_instance.create_google_business_place_action_with_http_info(account_id, create_google_business_place_action_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreateGoogleBusinessPlaceAction200Response>
rescue Late::ApiError => e
  puts "Error when calling GMBPlaceActionsApi->create_google_business_place_action_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |
| **create_google_business_place_action_request** | [**CreateGoogleBusinessPlaceActionRequest**](CreateGoogleBusinessPlaceActionRequest.md) |  |  |

### Return type

[**CreateGoogleBusinessPlaceAction200Response**](CreateGoogleBusinessPlaceAction200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_google_business_place_action

> <DeleteGoogleBusinessPlaceAction200Response> delete_google_business_place_action(account_id, name)

Delete a place action link

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::GMBPlaceActionsApi.new
account_id = 'account_id_example' # String | 
name = 'name_example' # String | The resource name of the place action link (e.g. locations/123/placeActionLinks/456)

begin
  # Delete a place action link
  result = api_instance.delete_google_business_place_action(account_id, name)
  p result
rescue Late::ApiError => e
  puts "Error when calling GMBPlaceActionsApi->delete_google_business_place_action: #{e}"
end
```

#### Using the delete_google_business_place_action_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeleteGoogleBusinessPlaceAction200Response>, Integer, Hash)> delete_google_business_place_action_with_http_info(account_id, name)

```ruby
begin
  # Delete a place action link
  data, status_code, headers = api_instance.delete_google_business_place_action_with_http_info(account_id, name)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeleteGoogleBusinessPlaceAction200Response>
rescue Late::ApiError => e
  puts "Error when calling GMBPlaceActionsApi->delete_google_business_place_action_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |
| **name** | **String** | The resource name of the place action link (e.g. locations/123/placeActionLinks/456) |  |

### Return type

[**DeleteGoogleBusinessPlaceAction200Response**](DeleteGoogleBusinessPlaceAction200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_google_business_place_actions

> <ListGoogleBusinessPlaceActions200Response> list_google_business_place_actions(account_id, opts)

List place action links (booking, ordering, reservations)

Lists place action links for a Google Business Profile location.  Place actions are the booking, ordering, and reservation buttons that appear on your listing. 

### Examples

```ruby
require 'time'
require 'late'
# setup authorization
Late.configure do |config|
  # Configure Bearer authorization (JWT): bearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Late::GMBPlaceActionsApi.new
account_id = 'account_id_example' # String | 
opts = {
  page_size: 56, # Integer | 
  page_token: 'page_token_example' # String | 
}

begin
  # List place action links (booking, ordering, reservations)
  result = api_instance.list_google_business_place_actions(account_id, opts)
  p result
rescue Late::ApiError => e
  puts "Error when calling GMBPlaceActionsApi->list_google_business_place_actions: #{e}"
end
```

#### Using the list_google_business_place_actions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListGoogleBusinessPlaceActions200Response>, Integer, Hash)> list_google_business_place_actions_with_http_info(account_id, opts)

```ruby
begin
  # List place action links (booking, ordering, reservations)
  data, status_code, headers = api_instance.list_google_business_place_actions_with_http_info(account_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListGoogleBusinessPlaceActions200Response>
rescue Late::ApiError => e
  puts "Error when calling GMBPlaceActionsApi->list_google_business_place_actions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |
| **page_size** | **Integer** |  | [optional][default to 100] |
| **page_token** | **String** |  | [optional] |

### Return type

[**ListGoogleBusinessPlaceActions200Response**](ListGoogleBusinessPlaceActions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

