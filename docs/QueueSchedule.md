# Late::QueueSchedule

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **_id** | **String** | Unique queue identifier | [optional] |
| **profile_id** | **String** | Profile ID this queue belongs to | [optional] |
| **name** | **String** | Queue name (e.g., \&quot;Morning Posts\&quot;, \&quot;Evening Content\&quot;) | [optional] |
| **timezone** | **String** | IANA timezone (e.g., America/New_York) | [optional] |
| **slots** | [**Array&lt;QueueSlot&gt;**](QueueSlot.md) |  | [optional] |
| **active** | **Boolean** | Whether the queue is active | [optional] |
| **is_default** | **Boolean** | Whether this is the default queue for the profile (used when no queueId specified) | [optional] |
| **created_at** | **Time** |  | [optional] |
| **updated_at** | **Time** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::QueueSchedule.new(
  _id: null,
  profile_id: null,
  name: null,
  timezone: null,
  slots: null,
  active: null,
  is_default: null,
  created_at: null,
  updated_at: null
)
```

