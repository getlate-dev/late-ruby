# Late::ListInboxConversations200ResponseDataInnerInstagramProfile

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **is_follower** | **Boolean** | Whether the participant follows your Instagram business account | [optional] |
| **is_following** | **Boolean** | Whether your Instagram business account follows the participant | [optional] |
| **follower_count** | **Integer** | The participant&#39;s follower count on Instagram | [optional] |
| **is_verified** | **Boolean** | Whether the participant is a verified Instagram user | [optional] |
| **fetched_at** | **Time** | When this profile data was last fetched from Instagram | [optional] |

## Example

```ruby
require 'late'

instance = Late::ListInboxConversations200ResponseDataInnerInstagramProfile.new(
  is_follower: null,
  is_following: null,
  follower_count: null,
  is_verified: null,
  fetched_at: null
)
```

