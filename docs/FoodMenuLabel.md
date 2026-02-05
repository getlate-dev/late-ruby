# Late::FoodMenuLabel

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **display_name** | **String** | Display name of the item/section/menu |  |
| **description** | **String** | Optional description | [optional] |
| **language_code** | **String** | BCP-47 language code (e.g. en, es) | [optional] |

## Example

```ruby
require 'late'

instance = Late::FoodMenuLabel.new(
  display_name: null,
  description: null,
  language_code: null
)
```

