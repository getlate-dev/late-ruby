# Late::SelectSnapchatProfileRequestSelectedPublicProfile

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Snapchat Public Profile ID |  |
| **display_name** | **String** | Display name of the public profile |  |
| **username** | **String** | Username/handle | [optional] |
| **profile_image_url** | **String** | Profile image URL | [optional] |
| **subscriber_count** | **Integer** | Number of subscribers | [optional] |

## Example

```ruby
require 'late'

instance = Late::SelectSnapchatProfileRequestSelectedPublicProfile.new(
  id: null,
  display_name: null,
  username: null,
  profile_image_url: null,
  subscriber_count: null
)
```

