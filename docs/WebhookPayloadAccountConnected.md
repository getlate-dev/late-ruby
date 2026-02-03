# Late::WebhookPayloadAccountConnected

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **event** | **String** |  | [optional] |
| **account** | [**WebhookPayloadAccountConnectedAccount**](WebhookPayloadAccountConnectedAccount.md) |  | [optional] |
| **timestamp** | **Time** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::WebhookPayloadAccountConnected.new(
  event: null,
  account: null,
  timestamp: null
)
```

