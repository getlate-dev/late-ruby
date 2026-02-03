# Late::GetAllAccountsHealth200ResponseAccountsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  | [optional] |
| **platform** | **String** |  | [optional] |
| **username** | **String** |  | [optional] |
| **display_name** | **String** |  | [optional] |
| **profile_id** | **String** |  | [optional] |
| **status** | **String** |  | [optional] |
| **can_post** | **Boolean** |  | [optional] |
| **can_fetch_analytics** | **Boolean** |  | [optional] |
| **token_valid** | **Boolean** |  | [optional] |
| **token_expires_at** | **Time** |  | [optional] |
| **needs_reconnect** | **Boolean** |  | [optional] |
| **issues** | **Array&lt;String&gt;** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetAllAccountsHealth200ResponseAccountsInner.new(
  account_id: null,
  platform: null,
  username: null,
  display_name: null,
  profile_id: null,
  status: null,
  can_post: null,
  can_fetch_analytics: null,
  token_valid: null,
  token_expires_at: null,
  needs_reconnect: null,
  issues: null
)
```

