# Late::ListLinkedInOrganizations200ResponseOrganizationsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Organization ID | [optional] |
| **logo_url** | **String** | Logo URL (may be absent if no logo) | [optional] |
| **vanity_name** | **String** | Organization&#39;s vanity name/slug | [optional] |
| **website** | **String** | Organization&#39;s website URL | [optional] |
| **industry** | **String** | Organization&#39;s primary industry | [optional] |
| **description** | **String** | Organization&#39;s description | [optional] |

## Example

```ruby
require 'late'

instance = Late::ListLinkedInOrganizations200ResponseOrganizationsInner.new(
  id: null,
  logo_url: null,
  vanity_name: null,
  website: null,
  industry: null,
  description: null
)
```

