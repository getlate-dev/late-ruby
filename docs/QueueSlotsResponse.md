# Late::QueueSlotsResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **exists** | **Boolean** |  | [optional] |
| **schedule** | [**QueueSchedule**](QueueSchedule.md) |  | [optional] |
| **next_slots** | **Array&lt;Time&gt;** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::QueueSlotsResponse.new(
  exists: null,
  schedule: null,
  next_slots: null
)
```

