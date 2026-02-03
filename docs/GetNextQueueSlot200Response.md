# Late::GetNextQueueSlot200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** |  | [optional] |
| **next_slot** | **Time** |  | [optional] |
| **timezone** | **String** |  | [optional] |
| **queue_id** | **String** | Queue ID this slot belongs to | [optional] |
| **queue_name** | **String** | Queue name | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetNextQueueSlot200Response.new(
  profile_id: null,
  next_slot: null,
  timezone: null,
  queue_id: null,
  queue_name: null
)
```

