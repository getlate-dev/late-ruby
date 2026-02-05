# Late::FoodMenu

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **labels** | [**Array&lt;FoodMenuLabel&gt;**](FoodMenuLabel.md) |  |  |
| **sections** | [**Array&lt;FoodMenuSection&gt;**](FoodMenuSection.md) |  | [optional] |
| **cuisines** | **Array&lt;String&gt;** | Cuisine types (e.g. AMERICAN, ITALIAN, JAPANESE) | [optional] |
| **source_url** | **String** | URL of the original menu source | [optional] |

## Example

```ruby
require 'late'

instance = Late::FoodMenu.new(
  labels: null,
  sections: null,
  cuisines: null,
  source_url: null
)
```

