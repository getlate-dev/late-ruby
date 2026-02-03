# Late::CreateQueueSlotRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** | Profile ID |  |
| **name** | **String** | Queue name (e.g., Evening Posts) |  |
| **timezone** | **String** | IANA timezone |  |
| **slots** | [**Array&lt;QueueSlot&gt;**](QueueSlot.md) |  |  |
| **active** | **Boolean** |  | [optional][default to true] |

## Example

```ruby
require 'late'

instance = Late::CreateQueueSlotRequest.new(
  profile_id: null,
  name: null,
  timezone: null,
  slots: null,
  active: null
)
```

