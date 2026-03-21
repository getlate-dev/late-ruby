# Late::GetTikTokCreatorInfo200ResponseCreator

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **nickname** | **String** | Creator display name | [optional] |
| **avatar_url** | **String** | Creator avatar URL | [optional] |
| **is_verified** | **Boolean** | Whether the creator is verified | [optional] |
| **can_post_more** | **Boolean** | Whether the creator can publish more posts right now | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::GetTikTokCreatorInfo200ResponseCreator.new(
  nickname: null,
  avatar_url: null,
  is_verified: null,
  can_post_more: null
)
```

