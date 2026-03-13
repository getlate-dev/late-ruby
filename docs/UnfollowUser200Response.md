# Late::UnfollowUser200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** |  | [optional] |
| **target_user_id** | **String** |  | [optional] |
| **following** | **Boolean** |  | [optional] |
| **platform** | **String** |  | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::UnfollowUser200Response.new(
  status: success,
  target_user_id: null,
  following: false,
  platform: twitter
)
```

