# Late::ListSequenceEnrollments200ResponseEnrollmentsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  | [optional] |
| **contact_id** | **String** |  | [optional] |
| **channel_id** | **String** |  | [optional] |
| **platform_identifier** | **String** |  | [optional] |
| **contact_name** | **String** |  | [optional] |
| **current_step_index** | **Integer** |  | [optional] |
| **status** | **String** |  | [optional] |
| **exit_reason** | **String** |  | [optional] |
| **next_step_at** | **Time** |  | [optional] |
| **steps_sent** | **Integer** |  | [optional] |
| **last_step_sent_at** | **Time** |  | [optional] |
| **created_at** | **Time** |  | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::ListSequenceEnrollments200ResponseEnrollmentsInner.new(
  id: null,
  contact_id: null,
  channel_id: null,
  platform_identifier: null,
  contact_name: null,
  current_step_index: null,
  status: null,
  exit_reason: null,
  next_step_at: null,
  steps_sent: null,
  last_step_sent_at: null,
  created_at: null
)
```

