# Late::WebhookLog

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **_id** | **String** |  | [optional] |
| **webhook_id** | **String** | ID of the webhook that was triggered | [optional] |
| **webhook_name** | **String** | Name of the webhook that was triggered | [optional] |
| **event** | **String** |  | [optional] |
| **url** | **String** |  | [optional] |
| **status** | **String** |  | [optional] |
| **status_code** | **Integer** | HTTP status code from webhook endpoint | [optional] |
| **request_payload** | **Object** | Payload sent to webhook endpoint | [optional] |
| **response_body** | **String** | Response body from webhook endpoint (truncated to 10KB) | [optional] |
| **error_message** | **String** | Error message if delivery failed | [optional] |
| **attempt_number** | **Integer** | Delivery attempt number (max 3 retries) | [optional] |
| **response_time** | **Integer** | Response time in milliseconds | [optional] |
| **created_at** | **Time** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::WebhookLog.new(
  _id: null,
  webhook_id: null,
  webhook_name: null,
  event: null,
  url: null,
  status: null,
  status_code: null,
  request_payload: null,
  response_body: null,
  error_message: null,
  attempt_number: null,
  response_time: null,
  created_at: null
)
```

