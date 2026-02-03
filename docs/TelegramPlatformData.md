# Late::TelegramPlatformData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **parse_mode** | **String** | Text formatting mode for the message (default is HTML) | [optional] |
| **disable_web_page_preview** | **Boolean** | Disable link preview generation for URLs in the message | [optional] |
| **disable_notification** | **Boolean** | Send the message silently (users will receive notification without sound) | [optional] |
| **protect_content** | **Boolean** | Protect message content from forwarding and saving | [optional] |

## Example

```ruby
require 'late'

instance = Late::TelegramPlatformData.new(
  parse_mode: null,
  disable_web_page_preview: null,
  disable_notification: null,
  protect_content: null
)
```

