# Late::CreateInviteToken201Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **token** | **String** |  | [optional] |
| **scope** | **String** |  | [optional] |
| **invited_profile_ids** | **Array&lt;String&gt;** |  | [optional] |
| **expires_at** | **Time** |  | [optional] |
| **invite_url** | **String** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::CreateInviteToken201Response.new(
  token: null,
  scope: null,
  invited_profile_ids: null,
  expires_at: null,
  invite_url: null
)
```

