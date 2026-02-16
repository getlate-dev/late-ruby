# Late::GoogleBusinessPlatformData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **location_id** | **String** | Target Google Business location ID for multi-location posting. Format: \&quot;locations/123456789\&quot; If omitted, uses the selected/default location on the connection. Use GET /api/v1/accounts/{id}/gmb-locations to list available locations.  | [optional] |
| **language_code** | **String** | BCP 47 language code for the post content (e.g., \&quot;en\&quot;, \&quot;de\&quot;, \&quot;es\&quot;, \&quot;fr\&quot;). If omitted, the language is automatically detected from the post text. Setting this explicitly is recommended when auto-detection may not be accurate (e.g., very short posts, mixed-language content, or transliterated text).  | [optional] |
| **call_to_action** | [**GoogleBusinessPlatformDataCallToAction**](GoogleBusinessPlatformDataCallToAction.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::GoogleBusinessPlatformData.new(
  location_id: null,
  language_code: de,
  call_to_action: null
)
```

