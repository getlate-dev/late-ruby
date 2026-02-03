# Late::ListInboxComments200ResponseDataInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  | [optional] |
| **platform** | **String** |  | [optional] |
| **account_id** | **String** |  | [optional] |
| **account_username** | **String** |  | [optional] |
| **content** | **String** |  | [optional] |
| **picture** | **String** |  | [optional] |
| **permalink** | **String** |  | [optional] |
| **created_time** | **Time** |  | [optional] |
| **comment_count** | **Integer** |  | [optional] |
| **like_count** | **Integer** |  | [optional] |
| **cid** | **String** | Bluesky content identifier | [optional] |
| **subreddit** | **String** | Reddit subreddit name | [optional] |

## Example

```ruby
require 'late'

instance = Late::ListInboxComments200ResponseDataInner.new(
  id: null,
  platform: null,
  account_id: null,
  account_username: null,
  content: null,
  picture: null,
  permalink: null,
  created_time: null,
  comment_count: null,
  like_count: null,
  cid: null,
  subreddit: null
)
```

