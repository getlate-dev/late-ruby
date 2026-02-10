# Late::ConnectionLogSuccess

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **display_name** | **String** |  | [optional] |
| **username** | **String** |  | [optional] |
| **profile_picture** | **String** |  | [optional] |
| **permissions** | **Array&lt;String&gt;** | OAuth scopes/permissions granted | [optional] |
| **token_expires_at** | **Time** |  | [optional] |
| **account_type** | **String** | Account type (personal, business, organization) | [optional] |

## Example

```ruby
require 'late'

instance = Late::ConnectionLogSuccess.new(
  display_name: null,
  username: null,
  profile_picture: null,
  permissions: null,
  token_expires_at: null,
  account_type: null
)
```

