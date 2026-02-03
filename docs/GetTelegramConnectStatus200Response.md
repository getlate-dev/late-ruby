# Late::GetTelegramConnectStatus200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **code** | **String** | The access code to send to the Telegram bot | [optional] |
| **expires_at** | **Time** | When the code expires | [optional] |
| **expires_in** | **Integer** | Seconds until expiration | [optional] |
| **bot_username** | **String** | The Telegram bot username to message | [optional] |
| **instructions** | **Array&lt;String&gt;** | Step-by-step connection instructions | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetTelegramConnectStatus200Response.new(
  code: LATE-ABC123,
  expires_at: null,
  expires_in: 900,
  bot_username: LateScheduleBot,
  instructions: null
)
```

