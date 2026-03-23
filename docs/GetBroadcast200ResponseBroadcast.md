# Late::GetBroadcast200ResponseBroadcast

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  | [optional] |
| **name** | **String** |  | [optional] |
| **description** | **String** |  | [optional] |
| **platform** | **String** |  | [optional] |
| **account_id** | **String** |  | [optional] |
| **message** | [**GetBroadcast200ResponseBroadcastMessage**](GetBroadcast200ResponseBroadcastMessage.md) |  | [optional] |
| **template** | [**GetWhatsAppBroadcasts200ResponseBroadcastsInnerTemplate**](GetWhatsAppBroadcasts200ResponseBroadcastsInnerTemplate.md) |  | [optional] |
| **segment_filters** | [**GetBroadcast200ResponseBroadcastSegmentFilters**](GetBroadcast200ResponseBroadcastSegmentFilters.md) |  | [optional] |
| **status** | **String** |  | [optional] |
| **scheduled_at** | **Time** |  | [optional] |
| **started_at** | **Time** |  | [optional] |
| **completed_at** | **Time** |  | [optional] |
| **recipient_count** | **Integer** |  | [optional] |
| **sent_count** | **Integer** |  | [optional] |
| **delivered_count** | **Integer** |  | [optional] |
| **read_count** | **Integer** |  | [optional] |
| **failed_count** | **Integer** |  | [optional] |
| **created_at** | **Time** |  | [optional] |
| **updated_at** | **Time** |  | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::GetBroadcast200ResponseBroadcast.new(
  id: null,
  name: null,
  description: null,
  platform: null,
  account_id: null,
  message: null,
  template: null,
  segment_filters: null,
  status: null,
  scheduled_at: null,
  started_at: null,
  completed_at: null,
  recipient_count: null,
  sent_count: null,
  delivered_count: null,
  read_count: null,
  failed_count: null,
  created_at: null,
  updated_at: null
)
```

