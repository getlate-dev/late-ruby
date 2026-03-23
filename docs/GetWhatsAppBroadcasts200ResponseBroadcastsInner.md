# Late::GetWhatsAppBroadcasts200ResponseBroadcastsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  | [optional] |
| **name** | **String** |  | [optional] |
| **description** | **String** |  | [optional] |
| **template** | [**GetWhatsAppBroadcasts200ResponseBroadcastsInnerTemplate**](GetWhatsAppBroadcasts200ResponseBroadcastsInnerTemplate.md) |  | [optional] |
| **status** | **String** |  | [optional] |
| **message_preview** | **String** | Template name or message text snippet | [optional] |
| **recipient_count** | **Integer** |  | [optional] |
| **scheduled_at** | **Time** |  | [optional] |
| **started_at** | **Time** |  | [optional] |
| **completed_at** | **Time** |  | [optional] |
| **sent_count** | **Integer** |  | [optional] |
| **delivered_count** | **Integer** |  | [optional] |
| **read_count** | **Integer** |  | [optional] |
| **failed_count** | **Integer** |  | [optional] |
| **created_at** | **Time** |  | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::GetWhatsAppBroadcasts200ResponseBroadcastsInner.new(
  id: null,
  name: null,
  description: null,
  template: null,
  status: null,
  message_preview: null,
  recipient_count: null,
  scheduled_at: null,
  started_at: null,
  completed_at: null,
  sent_count: null,
  delivered_count: null,
  read_count: null,
  failed_count: null,
  created_at: null
)
```

