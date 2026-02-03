# Late::WebhookPayloadAccountDisconnected

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **event** | **String** |  | [optional] |
| **account** | [**WebhookPayloadAccountDisconnectedAccount**](WebhookPayloadAccountDisconnectedAccount.md) |  | [optional] |
| **timestamp** | **Time** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::WebhookPayloadAccountDisconnected.new(
  event: null,
  account: null,
  timestamp: null
)
```

