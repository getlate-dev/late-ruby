# Late::AccountWithFollowerStats

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
| **profile_picture** | **String** |  | [optional] |
| **current_followers** | **Float** | Current follower count | [optional] |
| **last_updated** | **Time** |  | [optional] |
| **growth** | **Float** | Follower change over period | [optional] |
| **growth_percentage** | **Float** | Percentage growth | [optional] |
| **data_points** | **Float** | Number of historical snapshots | [optional] |

## Example

```ruby
require 'late'

instance = Late::AccountWithFollowerStats.new(
  _id: null,
  platform: null,
  profile_id: null,
  username: null,
  display_name: null,
  profile_url: null,
  is_active: null,
  followers_count: null,
  followers_last_updated: null,
  profile_picture: null,
  current_followers: null,
  last_updated: null,
  growth: null,
  growth_percentage: null,
  data_points: null
)
```

