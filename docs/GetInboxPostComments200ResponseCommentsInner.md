# Late::GetInboxPostComments200ResponseCommentsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  | [optional] |
| **message** | **String** |  | [optional] |
| **created_time** | **Time** |  | [optional] |
| **from** | [**GetInboxPostComments200ResponseCommentsInnerFrom**](GetInboxPostComments200ResponseCommentsInnerFrom.md) |  | [optional] |
| **like_count** | **Integer** |  | [optional] |
| **reply_count** | **Integer** |  | [optional] |
| **platform** | **String** | The platform this comment is from | [optional] |
| **url** | **String** | Direct link to the comment on the platform (if available) | [optional] |
| **replies** | **Array&lt;Object&gt;** |  | [optional] |
| **can_reply** | **Boolean** |  | [optional] |
| **can_delete** | **Boolean** |  | [optional] |
| **can_hide** | **Boolean** | Whether this comment can be hidden (Facebook | [optional] |
| **can_like** | **Boolean** | Whether this comment can be liked (Facebook | [optional] |
| **is_hidden** | **Boolean** | Whether the comment is currently hidden | [optional] |
| **is_liked** | **Boolean** | Whether the current user has liked this comment | [optional] |
| **like_uri** | **String** | Bluesky like URI for unliking | [optional] |
| **cid** | **String** | Bluesky content identifier | [optional] |
| **parent_id** | **String** | Parent comment ID for nested replies | [optional] |
| **root_uri** | **String** | Bluesky root post URI | [optional] |
| **root_cid** | **String** | Bluesky root post CID | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetInboxPostComments200ResponseCommentsInner.new(
  id: null,
  message: null,
  created_time: null,
  from: null,
  like_count: null,
  reply_count: null,
  platform: null,
  url: null,
  replies: null,
  can_reply: null,
  can_delete: null,
  can_hide: null,
  can_like: null,
  is_hidden: null,
  is_liked: null,
  like_uri: null,
  cid: null,
  parent_id: null,
  root_uri: null,
  root_cid: null
)
```

