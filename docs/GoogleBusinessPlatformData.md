# Late::GoogleBusinessPlatformData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **location_id** | **String** | Target Google Business location ID for multi-location posting. Format: \&quot;locations/123456789\&quot; If omitted, uses the selected/default location on the connection. Use GET /api/v1/accounts/{id}/gmb-locations to list available locations.  | [optional] |
| **call_to_action** | [**GoogleBusinessPlatformDataCallToAction**](GoogleBusinessPlatformDataCallToAction.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::GoogleBusinessPlatformData.new(
  location_id: null,
  call_to_action: null
)
```

