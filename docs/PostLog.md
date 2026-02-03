# Late::PostLog

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **_id** | **String** |  | [optional] |
| **post_id** | [**PostLogPostId**](PostLogPostId.md) |  | [optional] |
| **user_id** | **String** |  | [optional] |
| **profile_id** | **String** |  | [optional] |
| **platform** | **String** |  | [optional] |
| **account_id** | **String** |  | [optional] |
| **account_username** | **String** |  | [optional] |
| **action** | **String** | Type of action logged: - &#x60;publish&#x60; - Initial publish attempt - &#x60;retry&#x60; - Retry after failure - &#x60;media_upload&#x60; - Media upload step - &#x60;rate_limit_pause&#x60; - Account paused due to rate limits - &#x60;token_refresh&#x60; - Token was refreshed - &#x60;cancelled&#x60; - Post was cancelled  | [optional] |
| **status** | **String** |  | [optional] |
| **status_code** | **Integer** | HTTP status code from platform API | [optional] |
| **endpoint** | **String** | Platform API endpoint called | [optional] |
| **request** | [**PostLogRequest**](PostLogRequest.md) |  | [optional] |
| **response** | [**PostLogResponse**](PostLogResponse.md) |  | [optional] |
| **duration_ms** | **Integer** | How long the operation took in milliseconds | [optional] |
| **attempt_number** | **Integer** | Attempt number (1 for first try, 2+ for retries) | [optional] |
| **created_at** | **Time** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::PostLog.new(
  _id: null,
  post_id: null,
  user_id: null,
  profile_id: null,
  platform: null,
  account_id: null,
  account_username: null,
  action: null,
  status: null,
  status_code: null,
  endpoint: null,
  request: null,
  response: null,
  duration_ms: null,
  attempt_number: null,
  created_at: null
)
```

