# Late::QueueUpdateResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **success** | **Boolean** |  | [optional] |
| **schedule** | [**QueueSchedule**](QueueSchedule.md) |  | [optional] |
| **next_slots** | **Array&lt;Time&gt;** |  | [optional] |
| **reshuffled_count** | **Integer** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::QueueUpdateResponse.new(
  success: null,
  schedule: null,
  next_slots: null,
  reshuffled_count: null
)
```

