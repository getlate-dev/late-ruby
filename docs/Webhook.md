# Late::Webhook

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **_id** | **String** | Unique webhook identifier | [optional] |
| **name** | **String** | Webhook name (for identification) | [optional] |
| **url** | **String** | Webhook endpoint URL | [optional] |
| **secret** | **String** | Secret key for HMAC-SHA256 signature (not returned in responses for security) | [optional] |
| **events** | **Array&lt;String&gt;** | Events subscribed to | [optional] |
| **is_active** | **Boolean** | Whether webhook delivery is enabled | [optional] |
| **last_fired_at** | **Time** | Timestamp of last successful webhook delivery | [optional] |
| **failure_count** | **Integer** | Consecutive delivery failures (resets on success, webhook disabled at 10) | [optional] |
| **custom_headers** | **Hash&lt;String, String&gt;** | Custom headers included in webhook requests | [optional] |

## Example

```ruby
require 'late'

instance = Late::Webhook.new(
  _id: null,
  name: null,
  url: null,
  secret: null,
  events: null,
  is_active: null,
  last_fired_at: null,
  failure_count: null,
  custom_headers: null
)
```

