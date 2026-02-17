# Late::InstagramPlatformData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **content_type** | **String** | Set to &#39;story&#39; to publish as a Story. Default posts become Reels or feed depending on media. | [optional] |
| **share_to_feed** | **Boolean** | For Reels only. When true (default), the Reel appears on both the Reels tab and your main profile feed. Set to false to post to the Reels tab only. | [optional][default to true] |
| **collaborators** | **Array&lt;String&gt;** | Up to 3 Instagram usernames to invite as collaborators (feed/Reels only) | [optional] |
| **first_comment** | **String** | Optional first comment to add after the post is created (not applied to Stories) | [optional] |
| **trial_params** | [**InstagramPlatformDataTrialParams**](InstagramPlatformDataTrialParams.md) |  | [optional] |
| **user_tags** | [**Array&lt;InstagramPlatformDataUserTagsInner&gt;**](InstagramPlatformDataUserTagsInner.md) | Tag Instagram users in photos by username and position. Not supported for stories or videos. For carousels, use mediaIndex to target specific slides (defaults to 0). Tags on video items are silently skipped. | [optional] |
| **audio_name** | **String** | Custom name for original audio in Reels. Replaces the default \&quot;Original Audio\&quot; label. Can only be set once. | [optional] |
| **thumb_offset** | **Integer** | Millisecond offset from video start for the Reel thumbnail. Ignored if a custom thumbnail URL is provided. Defaults to 0. | [optional] |

## Example

```ruby
require 'late'

instance = Late::InstagramPlatformData.new(
  content_type: null,
  share_to_feed: null,
  collaborators: null,
  first_comment: null,
  trial_params: null,
  user_tags: null,
  audio_name: My Podcast Intro,
  thumb_offset: 5000
)
```

