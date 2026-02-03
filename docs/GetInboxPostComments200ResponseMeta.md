# Late::GetInboxPostComments200ResponseMeta

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **platform** | **String** |  | [optional] |
| **post_id** | **String** |  | [optional] |
| **account_id** | **String** |  | [optional] |
| **subreddit** | **String** | (Reddit only) Subreddit name | [optional] |
| **last_updated** | **Time** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetInboxPostComments200ResponseMeta.new(
  platform: null,
  post_id: null,
  account_id: null,
  subreddit: null,
  last_updated: null
)
```

