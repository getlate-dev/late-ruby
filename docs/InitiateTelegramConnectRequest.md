# Late::InitiateTelegramConnectRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **chat_id** | **String** | The Telegram chat ID. Can be: - Numeric ID (e.g., \&quot;-1001234567890\&quot;) - Username with @ prefix (e.g., \&quot;@mychannel\&quot;)  |  |
| **profile_id** | **String** | The profile ID to connect the account to |  |

## Example

```ruby
require 'late'

instance = Late::InitiateTelegramConnectRequest.new(
  chat_id: null,
  profile_id: null
)
```

