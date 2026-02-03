# Late::TikTokPlatformData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **draft** | **Boolean** | When true, Late sends the post to the TikTok Creator Inbox as a draft instead of publishing it immediately. When omitted or false, TikTok uses direct posting (live publish) as usual.  | [optional] |
| **privacy_level** | **String** | One of the values returned by the TikTok creator info API for the account | [optional] |
| **allow_comment** | **Boolean** | Allow comments on the post | [optional] |
| **allow_duet** | **Boolean** | Allow duets (required for video posts) | [optional] |
| **allow_stitch** | **Boolean** | Allow stitches (required for video posts) | [optional] |
| **commercial_content_type** | **String** | Type of commercial content disclosure | [optional] |
| **brand_partner_promote** | **Boolean** | Whether the post promotes a brand partner | [optional] |
| **is_brand_organic_post** | **Boolean** | Whether the post is a brand organic post | [optional] |
| **content_preview_confirmed** | **Boolean** | User has confirmed they previewed the content | [optional] |
| **express_consent_given** | **Boolean** | User has given express consent for posting | [optional] |
| **media_type** | **String** | Optional override. Defaults based on provided media items. | [optional] |
| **video_cover_timestamp_ms** | **Integer** | Optional for video posts. Timestamp in milliseconds to select which frame to use as thumbnail (defaults to 1000ms/1 second). | [optional] |
| **photo_cover_index** | **Integer** | Optional for photo carousels. Index of image to use as cover, 0-based (defaults to 0/first image). | [optional] |
| **auto_add_music** | **Boolean** | When true, TikTok may add recommended music (photos only) | [optional] |
| **video_made_with_ai** | **Boolean** | Set true to disclose AI-generated content | [optional] |
| **description** | **String** | Optional long-form description for photo posts (max 4000 chars). Recommended for photo posts when content exceeds 90 characters, as photo titles are automatically truncated to 90 chars (after stripping hashtags/URLs).  | [optional] |

## Example

```ruby
require 'late'

instance = Late::TikTokPlatformData.new(
  draft: null,
  privacy_level: null,
  allow_comment: null,
  allow_duet: null,
  allow_stitch: null,
  commercial_content_type: null,
  brand_partner_promote: null,
  is_brand_organic_post: null,
  content_preview_confirmed: null,
  express_consent_given: null,
  media_type: null,
  video_cover_timestamp_ms: null,
  photo_cover_index: null,
  auto_add_music: null,
  video_made_with_ai: null,
  description: null
)
```

