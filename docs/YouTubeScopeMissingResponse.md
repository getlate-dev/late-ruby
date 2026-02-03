# Late::YouTubeScopeMissingResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **success** | **Boolean** |  | [optional] |
| **error** | **String** |  | [optional] |
| **code** | **String** |  | [optional] |
| **scope_status** | [**YouTubeScopeMissingResponseScopeStatus**](YouTubeScopeMissingResponseScopeStatus.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::YouTubeScopeMissingResponse.new(
  success: false,
  error: To access daily video analytics, please reconnect your YouTube account to grant the required permissions.,
  code: youtube_analytics_scope_missing,
  scope_status: null
)
```

