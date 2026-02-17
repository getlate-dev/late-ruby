# Late::PlatformTarget

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **platform** | **String** | Supported values: twitter, threads, instagram, youtube, facebook, linkedin, pinterest, reddit, tiktok, bluesky, googlebusiness, telegram | [optional] |
| **account_id** | [**PlatformTargetAccountId**](PlatformTargetAccountId.md) |  | [optional] |
| **custom_content** | **String** | Platform-specific text override. When set, this content is used instead of the top-level post content for this platform. Useful for tailoring captions per platform (e.g. keeping tweets under 280 characters). | [optional] |
| **custom_media** | [**Array&lt;MediaItem&gt;**](MediaItem.md) |  | [optional] |
| **scheduled_for** | **Time** | Optional per-platform scheduled time override (uses post.scheduledFor when omitted) | [optional] |
| **platform_specific_data** | [**PlatformTargetPlatformSpecificData**](PlatformTargetPlatformSpecificData.md) |  | [optional] |
| **status** | **String** | Platform-specific status: pending, publishing, published, failed | [optional] |
| **platform_post_id** | **String** | The native post ID on the platform (populated after successful publish) | [optional] |
| **platform_post_url** | **String** | Public URL of the published post on the platform. Populated after successful publish. For immediate posts (publishNow&#x3D;true),  this is included in the response. For scheduled posts, fetch the post  via GET /v1/posts/{postId} after the scheduled time.  | [optional] |
| **published_at** | **Time** | Timestamp when the post was published to this platform | [optional] |
| **error_message** | **String** | Human-readable error message when status is failed. Contains platform-specific error details explaining why the publish failed. | [optional] |
| **error_category** | **String** | Error category for programmatic handling: auth_expired (token expired/revoked), user_content (wrong format/too long), user_abuse (rate limits/spam), account_issue (config problems), platform_rejected (policy violation), platform_error (5xx/maintenance), system_error (Late infra), unknown | [optional] |
| **error_source** | **String** | Who caused the error: user (fix content/reconnect), platform (outage/API change), system (Late issue, rare) | [optional] |

## Example

```ruby
require 'late'

instance = Late::PlatformTarget.new(
  platform: twitter,
  account_id: null,
  custom_content: null,
  custom_media: null,
  scheduled_for: null,
  platform_specific_data: null,
  status: pending,
  platform_post_id: 1234567890123456789,
  platform_post_url: https://twitter.com/acmecorp/status/1234567890123456789,
  published_at: null,
  error_message: null,
  error_category: null,
  error_source: null
)
```

