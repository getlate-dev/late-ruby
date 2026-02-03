# Late::ReplyToInboxPostRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |
| **message** | **String** |  |  |
| **comment_id** | **String** | Reply to specific comment (optional) | [optional] |
| **subreddit** | **String** | (Reddit only) Subreddit name for replies | [optional] |
| **parent_cid** | **String** | (Bluesky only) Parent content identifier | [optional] |
| **root_uri** | **String** | (Bluesky only) Root post URI | [optional] |
| **root_cid** | **String** | (Bluesky only) Root post CID | [optional] |

## Example

```ruby
require 'late'

instance = Late::ReplyToInboxPostRequest.new(
  account_id: null,
  message: null,
  comment_id: null,
  subreddit: null,
  parent_cid: null,
  root_uri: null,
  root_cid: null
)
```

