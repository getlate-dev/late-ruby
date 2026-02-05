# Late::UpdateGoogleBusinessFoodMenusRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **menus** | [**Array&lt;FoodMenu&gt;**](FoodMenu.md) | Array of food menus to set |  |
| **update_mask** | **String** | Field mask for partial updates (e.g. \&quot;menus\&quot;) | [optional] |

## Example

```ruby
require 'late'

instance = Late::UpdateGoogleBusinessFoodMenusRequest.new(
  menus: null,
  update_mask: null
)
```

