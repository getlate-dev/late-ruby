# Late::UpdateQueueSlotRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** |  |  |
| **queue_id** | **String** | Queue ID to update (optional) | [optional] |
| **name** | **String** | Queue name | [optional] |
| **timezone** | **String** |  |  |
| **slots** | [**Array&lt;QueueSlot&gt;**](QueueSlot.md) |  |  |
| **active** | **Boolean** |  | [optional][default to true] |
| **set_as_default** | **Boolean** | Make this queue the default | [optional] |
| **reshuffle_existing** | **Boolean** | Whether to reschedule existing queued posts to match new slots | [optional][default to false] |

## Example

```ruby
require 'late'

instance = Late::UpdateQueueSlotRequest.new(
  profile_id: null,
  queue_id: null,
  name: null,
  timezone: null,
  slots: null,
  active: null,
  set_as_default: null,
  reshuffle_existing: null
)
```

