# Late::CreateQueueSlot201Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **success** | **Boolean** |  | [optional] |
| **schedule** | [**QueueSchedule**](QueueSchedule.md) |  | [optional] |
| **next_slots** | **Array&lt;Time&gt;** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::CreateQueueSlot201Response.new(
  success: null,
  schedule: null,
  next_slots: null
)
```

