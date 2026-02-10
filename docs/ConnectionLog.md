# Late::ConnectionLog

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **_id** | **String** |  | [optional] |
| **user_id** | **String** | User who owns the connection (may be null for early OAuth failures) | [optional] |
| **profile_id** | **String** |  | [optional] |
| **account_id** | **String** | The social account ID (present on successful connections and disconnects) | [optional] |
| **platform** | **String** |  | [optional] |
| **event_type** | **String** | Type of connection event: - &#x60;connect_success&#x60; - New account connected successfully - &#x60;connect_failed&#x60; - Connection attempt failed - &#x60;disconnect&#x60; - Account was disconnected - &#x60;reconnect_success&#x60; - Existing account reconnected successfully - &#x60;reconnect_failed&#x60; - Reconnection attempt failed  | [optional] |
| **connection_method** | **String** | How the connection was initiated | [optional] |
| **error** | [**ConnectionLogError**](ConnectionLogError.md) |  | [optional] |
| **success** | [**ConnectionLogSuccess**](ConnectionLogSuccess.md) |  | [optional] |
| **context** | [**ConnectionLogContext**](ConnectionLogContext.md) |  | [optional] |
| **duration_ms** | **Integer** | How long the operation took in milliseconds | [optional] |
| **metadata** | **Object** | Additional metadata | [optional] |
| **created_at** | **Time** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::ConnectionLog.new(
  _id: null,
  user_id: null,
  profile_id: null,
  account_id: null,
  platform: null,
  event_type: null,
  connection_method: null,
  error: null,
  success: null,
  context: null,
  duration_ms: null,
  metadata: null,
  created_at: null
)
```

