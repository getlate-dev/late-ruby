# Late::GetSequence200ResponseSequence

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  | [optional] |
| **name** | **String** |  | [optional] |
| **description** | **String** |  | [optional] |
| **platform** | **String** |  | [optional] |
| **account_id** | **String** |  | [optional] |
| **status** | **String** |  | [optional] |
| **steps** | [**Array&lt;GetSequence200ResponseSequenceStepsInner&gt;**](GetSequence200ResponseSequenceStepsInner.md) |  | [optional] |
| **exit_on_reply** | **Boolean** |  | [optional] |
| **exit_on_unsubscribe** | **Boolean** |  | [optional] |
| **total_enrolled** | **Integer** |  | [optional] |
| **total_completed** | **Integer** |  | [optional] |
| **total_exited** | **Integer** |  | [optional] |
| **created_at** | **Time** |  | [optional] |
| **updated_at** | **Time** |  | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::GetSequence200ResponseSequence.new(
  id: null,
  name: null,
  description: null,
  platform: null,
  account_id: null,
  status: null,
  steps: null,
  exit_on_reply: null,
  exit_on_unsubscribe: null,
  total_enrolled: null,
  total_completed: null,
  total_exited: null,
  created_at: null,
  updated_at: null
)
```

