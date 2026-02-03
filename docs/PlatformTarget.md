# Late::PlatformTarget

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **platform** | **String** | Supported values: twitter, threads, instagram, youtube, facebook, linkedin, pinterest, reddit, tiktok, bluesky, googlebusiness, telegram | [optional] |
| **account_id** | [**PlatformTargetAccountId**](PlatformTargetAccountId.md) |  | [optional] |
| **custom_content** | **String** |  | [optional] |
| **custom_media** | [**Array&lt;MediaItem&gt;**](MediaItem.md) |  | [optional] |
| **scheduled_for** | **Time** | Optional per-platform scheduled time override (uses post.scheduledFor when omitted) | [optional] |
| **platform_specific_data** | [**PlatformTargetPlatformSpecificData**](PlatformTargetPlatformSpecificData.md) |  | [optional] |
| **status** | **String** | Platform-specific status: pending, publishing, published, failed | [optional] |
| **platform_post_id** | **String** | The native post ID on the platform (populated after successful publish) | [optional] |
| **platform_post_url** | **String** | Public URL of the published post on the platform. Populated after successful publish. For immediate posts (publishNow&#x3D;true),  this is included in the response. For scheduled posts, fetch the post  via GET /v1/posts/{postId} after the scheduled time.  | [optional] |
| **published_at** | **Time** | Timestamp when the post was published to this platform | [optional] |
| **error_message** | **String** | Human-readable error message when status is &#39;failed&#39;. Contains platform-specific error details explaining why the publish failed. Examples: - \&quot;Instagram access token has expired. Please reconnect your account.\&quot; - \&quot;Post text exceeds the 500 character limit for Threads.\&quot; - \&quot;You do not have enough karma to post in this subreddit.\&quot; - \&quot;Video is too long for Reels. Facebook Reels must be 90 seconds or less.\&quot;  | [optional] |
| **error_category** | **String** | Error category for programmatic handling: - auth_expired: Token expired or revoked, account needs reconnection - user_content: Content doesn&#39;t meet platform requirements (too long, wrong format, etc.) - user_abuse: Rate limits, spam detection, excessive posting - account_issue: Account configuration problems (missing board, inactive account) - platform_rejected: Platform rules violated (banned, suspended, policy violation) - platform_error: Platform-side issues (5xx errors, maintenance) - system_error: Late infrastructure issues (timeouts, network errors) - unknown: Unclassified error  | [optional] |
| **error_source** | **String** | Who/what caused the error: - user: User action required (fix content, reconnect account) - platform: Platform-side issue (outage, API change) - system: Late system issue (rare)  | [optional] |

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

