# Late::FoodMenuItem

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **labels** | [**Array&lt;FoodMenuLabel&gt;**](FoodMenuLabel.md) |  |  |
| **attributes** | [**FoodMenuItemAttributes**](FoodMenuItemAttributes.md) |  | [optional] |
| **options** | [**Array&lt;FoodMenuItemOptionsInner&gt;**](FoodMenuItemOptionsInner.md) | Item variants/options (e.g. sizes, preparations) | [optional] |

## Example

```ruby
require 'late'

instance = Late::FoodMenuItem.new(
  labels: null,
  attributes: null,
  options: null
)
```

