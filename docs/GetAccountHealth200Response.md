# Late::GetAccountHealth200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  | [optional] |
| **platform** | **String** |  | [optional] |
| **username** | **String** |  | [optional] |
| **display_name** | **String** |  | [optional] |
| **status** | **String** | Overall health status | [optional] |
| **token_status** | [**GetAccountHealth200ResponseTokenStatus**](GetAccountHealth200ResponseTokenStatus.md) |  | [optional] |
| **permissions** | [**GetAccountHealth200ResponsePermissions**](GetAccountHealth200ResponsePermissions.md) |  | [optional] |
| **issues** | **Array&lt;String&gt;** | List of issues found | [optional] |
| **recommendations** | **Array&lt;String&gt;** | Actionable recommendations to fix issues | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetAccountHealth200Response.new(
  account_id: null,
  platform: null,
  username: null,
  display_name: null,
  status: null,
  token_status: null,
  permissions: null,
  issues: null,
  recommendations: null
)
```

