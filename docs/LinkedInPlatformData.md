# Late::LinkedInPlatformData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_title** | **String** | Title displayed on LinkedIn document (PDF/carousel) posts. Required by LinkedIn for document posts. If omitted, falls back to the media item title, then the filename. | [optional] |
| **organization_urn** | **String** | Target LinkedIn Organization URN (e.g. \&quot;urn:li:organization:123456789\&quot;). If omitted, uses the default org. Use GET /v1/accounts/{id}/linkedin-organizations to list orgs. | [optional] |
| **first_comment** | **String** | Optional first comment to add after the post is created | [optional] |
| **disable_link_preview** | **Boolean** | Set to true to disable automatic link previews for URLs in the post content (default is false) | [optional] |

## Example

```ruby
require 'late'

instance = Late::LinkedInPlatformData.new(
  document_title: null,
  organization_urn: null,
  first_comment: null,
  disable_link_preview: null
)
```

