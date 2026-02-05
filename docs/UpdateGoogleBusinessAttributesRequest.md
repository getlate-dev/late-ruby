# Late::UpdateGoogleBusinessAttributesRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **attributes** | [**Array&lt;UpdateGoogleBusinessAttributesRequestAttributesInner&gt;**](UpdateGoogleBusinessAttributesRequestAttributesInner.md) |  |  |
| **attribute_mask** | **String** | Comma-separated attribute names to update (e.g. &#39;has_delivery,has_takeout&#39;) |  |

## Example

```ruby
require 'late'

instance = Late::UpdateGoogleBusinessAttributesRequest.new(
  attributes: null,
  attribute_mask: null
)
```

