# Late::FollowUser200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** |  | [optional] |
| **target_user_id** | **String** |  | [optional] |
| **following** | **Boolean** |  | [optional] |
| **pending_follow** | **Boolean** | True if the target account is protected and a follow request was sent | [optional] |
| **platform** | **String** |  | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::FollowUser200Response.new(
  status: success,
  target_user_id: null,
  following: null,
  pending_follow: null,
  platform: twitter
)
```

