# Late::UpdateWebhookSettingsRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **_id** | **String** | Webhook ID to update (required) |  |
| **name** | **String** | Webhook name (max 50 characters) | [optional] |
| **url** | **String** | Webhook endpoint URL (must be HTTPS in production) | [optional] |
| **secret** | **String** | Secret key for HMAC-SHA256 signature verification | [optional] |
| **events** | **Array&lt;String&gt;** | Events to subscribe to | [optional] |
| **is_active** | **Boolean** | Enable or disable webhook delivery | [optional] |
| **custom_headers** | **Hash&lt;String, String&gt;** | Custom headers to include in webhook requests | [optional] |

## Example

```ruby
require 'late'

instance = Late::UpdateWebhookSettingsRequest.new(
  _id: null,
  name: null,
  url: null,
  secret: null,
  events: null,
  is_active: null,
  custom_headers: null
)
```

