# Late::GetGoogleBusinessFoodMenus200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **success** | **Boolean** |  | [optional] |
| **account_id** | **String** |  | [optional] |
| **location_id** | **String** |  | [optional] |
| **name** | **String** | Resource name of the food menus | [optional] |
| **menus** | [**Array&lt;FoodMenu&gt;**](FoodMenu.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetGoogleBusinessFoodMenus200Response.new(
  success: null,
  account_id: null,
  location_id: null,
  name: null,
  menus: null
)
```

