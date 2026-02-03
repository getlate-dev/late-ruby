# Late::LinkedInPlatformData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **organization_urn** | **String** | Target LinkedIn Organization URN for multi-organization posting. Format: \&quot;urn:li:organization:123456789\&quot; If omitted, uses the selected/default organization on the connection. Use GET /api/v1/accounts/{id}/linkedin-organizations to list available organizations.  | [optional] |
| **first_comment** | **String** | Optional first comment to add after the post is created | [optional] |
| **disable_link_preview** | **Boolean** | Set to true to disable automatic link previews for URLs in the post content (default is false) | [optional] |

## Example

```ruby
require 'late'

instance = Late::LinkedInPlatformData.new(
  organization_urn: null,
  first_comment: null,
  disable_link_preview: null
)
```

