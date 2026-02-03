# Late::PlatformAnalytics

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **platform** | **String** |  | [optional] |
| **status** | **String** |  | [optional] |
| **account_id** | **String** |  | [optional] |
| **account_username** | **String** |  | [optional] |
| **analytics** | [**PostAnalytics**](PostAnalytics.md) |  | [optional] |
| **account_metrics** | [**PlatformAnalyticsAccountMetrics**](PlatformAnalyticsAccountMetrics.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::PlatformAnalytics.new(
  platform: null,
  status: null,
  account_id: null,
  account_username: null,
  analytics: null,
  account_metrics: null
)
```

