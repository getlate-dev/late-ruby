# Late::ListQueueSlots200ResponseOneOf

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **exists** | **Boolean** |  | [optional] |
| **schedule** | [**QueueSchedule**](QueueSchedule.md) |  | [optional] |
| **next_slots** | **Array&lt;Time&gt;** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::ListQueueSlots200ResponseOneOf.new(
  exists: null,
  schedule: null,
  next_slots: null
)
```

