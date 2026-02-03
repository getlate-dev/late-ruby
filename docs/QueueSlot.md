# Late::QueueSlot

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **day_of_week** | **Integer** | Day of week (0&#x3D;Sunday, 6&#x3D;Saturday) | [optional] |
| **time** | **String** | Time in HH:mm format (24-hour) | [optional] |

## Example

```ruby
require 'late'

instance = Late::QueueSlot.new(
  day_of_week: null,
  time: null
)
```

