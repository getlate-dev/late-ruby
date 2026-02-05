# Late::FoodMenuItemAttributes

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **price** | [**Money**](Money.md) |  | [optional] |
| **spiciness** | **String** | Spiciness level (e.g. MILD, MEDIUM, HOT) | [optional] |
| **allergen** | **Array&lt;String&gt;** | Allergens (e.g. DAIRY, GLUTEN, SHELLFISH) | [optional] |
| **dietary_restriction** | **Array&lt;String&gt;** | Dietary labels (e.g. VEGETARIAN, VEGAN, GLUTEN_FREE) | [optional] |
| **serves_num_people** | **Integer** | Number of people the item serves | [optional] |
| **preparation_methods** | **Array&lt;String&gt;** | Preparation methods (e.g. GRILLED, FRIED) | [optional] |
| **media_keys** | **Array&lt;String&gt;** | Media references for item photos | [optional] |

## Example

```ruby
require 'late'

instance = Late::FoodMenuItemAttributes.new(
  price: null,
  spiciness: null,
  allergen: null,
  dietary_restriction: null,
  serves_num_people: null,
  preparation_methods: null,
  media_keys: null
)
```

