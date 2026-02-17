# Late::SocialAccount

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **_id** | **String** |  | [optional] |
| **platform** | **String** |  | [optional] |
| **profile_id** | [**SocialAccountProfileId**](SocialAccountProfileId.md) |  | [optional] |
| **username** | **String** |  | [optional] |
| **display_name** | **String** |  | [optional] |
| **profile_url** | **String** | Full profile URL for the connected account on its platform. | [optional] |
| **is_active** | **Boolean** |  | [optional] |
| **followers_count** | **Float** | Follower count (only included if user has analytics add-on) | [optional] |
| **followers_last_updated** | **Time** | Last time follower count was updated (only included if user has analytics add-on) | [optional] |

## Example

```ruby
require 'late'

instance = Late::SocialAccount.new(
  _id: null,
  platform: null,
  profile_id: null,
  username: null,
  display_name: null,
  profile_url: null,
  is_active: null,
  followers_count: null,
  followers_last_updated: null
)
```

