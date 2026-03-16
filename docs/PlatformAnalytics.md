# Late::PlatformAnalytics

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **platform** | **String** |  | [optional] |
| **status** | **String** |  | [optional] |
| **account_id** | **String** |  | [optional] |
| **account_username** | **String** |  | [optional] |
| **analytics** | [**PostAnalytics**](PostAnalytics.md) |  | [optional] |
| **sync_status** | **String** | Sync state of analytics for this platform | [optional] |
| **platform_post_url** | **String** |  | [optional] |
| **error_message** | **String** | Error details when status is failed | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::PlatformAnalytics.new(
  platform: null,
  status: null,
  account_id: null,
  account_username: null,
  analytics: null,
  sync_status: null,
  platform_post_url: null,
  error_message: null
)
```

