# Late::CreateInviteTokenRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **scope** | **String** | &#39;all&#39; grants access to all profiles, &#39;profiles&#39; restricts to specific profiles |  |
| **profile_ids** | **Array&lt;String&gt;** | Required if scope is &#39;profiles&#39;. Array of profile IDs to grant access to. | [optional] |

## Example

```ruby
require 'late'

instance = Late::CreateInviteTokenRequest.new(
  scope: null,
  profile_ids: null
)
```

