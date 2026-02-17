# Late::CreatePostRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **title** | **String** |  | [optional] |
| **content** | **String** | Post caption/text. Optional when media is attached or all platforms have customContent. Required for text-only posts. | [optional] |
| **media_items** | [**Array&lt;CreatePostRequestMediaItemsInner&gt;**](CreatePostRequestMediaItemsInner.md) |  | [optional] |
| **platforms** | [**Array&lt;CreatePostRequestPlatformsInner&gt;**](CreatePostRequestPlatformsInner.md) |  | [optional] |
| **scheduled_for** | **Time** |  | [optional] |
| **publish_now** | **Boolean** |  | [optional][default to false] |
| **is_draft** | **Boolean** |  | [optional][default to false] |
| **timezone** | **String** |  | [optional][default to &#39;UTC&#39;] |
| **tags** | **Array&lt;String&gt;** | Tags/keywords. YouTube constraints: each tag max 100 chars, combined max 500 chars, duplicates auto-removed. | [optional] |
| **hashtags** | **Array&lt;String&gt;** |  | [optional] |
| **mentions** | **Array&lt;String&gt;** |  | [optional] |
| **crossposting_enabled** | **Boolean** |  | [optional][default to true] |
| **metadata** | **Hash&lt;String, Object&gt;** |  | [optional] |
| **tiktok_settings** | [**TikTokPlatformData**](TikTokPlatformData.md) | Root-level TikTok settings applied to all TikTok platforms. Merged into each platform&#39;s platformSpecificData, with platform-specific settings taking precedence. | [optional] |
| **queued_from_profile** | **String** | Profile ID to schedule via queue. When provided without scheduledFor, the post is auto-assigned to the next available slot. Do not call /v1/queue/next-slot and use that time in scheduledFor, as that bypasses queue locking. | [optional] |
| **queue_id** | **String** | Specific queue ID to use when scheduling via queue. Only used when queuedFromProfile is also provided. If omitted, uses the profile&#39;s default queue.  | [optional] |

## Example

```ruby
require 'late'

instance = Late::CreatePostRequest.new(
  title: null,
  content: null,
  media_items: null,
  platforms: null,
  scheduled_for: null,
  publish_now: null,
  is_draft: null,
  timezone: null,
  tags: null,
  hashtags: null,
  mentions: null,
  crossposting_enabled: null,
  metadata: null,
  tiktok_settings: null,
  queued_from_profile: null,
  queue_id: null
)
```

