# Late::CreateSequenceRequestStepsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **order** | **Integer** |  |  |
| **delay_minutes** | **Integer** |  |  |
| **message** | [**GetBroadcast200ResponseBroadcastMessage**](GetBroadcast200ResponseBroadcastMessage.md) |  | [optional] |
| **template** | [**CreateSequenceRequestStepsInnerTemplate**](CreateSequenceRequestStepsInnerTemplate.md) |  | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::CreateSequenceRequestStepsInner.new(
  order: null,
  delay_minutes: null,
  message: null,
  template: null
)
```

