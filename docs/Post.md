# Late::Post

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **_id** | **String** |  | [optional] |
| **user_id** | [**PostUserId**](PostUserId.md) |  | [optional] |
| **title** | **String** | YouTube: title must be ≤ 100 characters.  | [optional] |
| **content** | **String** |  | [optional] |
| **media_items** | [**Array&lt;MediaItem&gt;**](MediaItem.md) |  | [optional] |
| **platforms** | [**Array&lt;PlatformTarget&gt;**](PlatformTarget.md) |  | [optional] |
| **scheduled_for** | **Time** |  | [optional] |
| **timezone** | **String** |  | [optional] |
| **status** | **String** |  | [optional] |
| **tags** | **Array&lt;String&gt;** | YouTube constraints: each tag max 100 chars, combined max 500 chars, duplicates removed. | [optional] |
| **hashtags** | **Array&lt;String&gt;** |  | [optional] |
| **mentions** | **Array&lt;String&gt;** |  | [optional] |
| **visibility** | **String** |  | [optional] |
| **metadata** | **Hash&lt;String, Object&gt;** |  | [optional] |
| **queued_from_profile** | **String** | Profile ID if the post was scheduled via the queue | [optional] |
| **queue_id** | **String** | Queue ID if the post was scheduled via a specific queue | [optional] |
| **created_at** | **Time** |  | [optional] |
| **updated_at** | **Time** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::Post.new(
  _id: null,
  user_id: null,
  title: null,
  content: null,
  media_items: null,
  platforms: null,
  scheduled_for: null,
  timezone: null,
  status: null,
  tags: null,
  hashtags: null,
  mentions: null,
  visibility: null,
  metadata: null,
  queued_from_profile: null,
  queue_id: null,
  created_at: null,
  updated_at: null
)
```

