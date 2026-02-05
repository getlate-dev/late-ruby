# Late::GetGoogleBusinessAttributes200ResponseAttributesInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Attribute identifier (e.g. has_delivery) | [optional] |
| **value_type** | **String** | Value type (BOOL, ENUM, URL, REPEATED_ENUM) | [optional] |
| **values** | **Array&lt;Object&gt;** |  | [optional] |
| **repeated_enum_value** | [**GetGoogleBusinessAttributes200ResponseAttributesInnerRepeatedEnumValue**](GetGoogleBusinessAttributes200ResponseAttributesInnerRepeatedEnumValue.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetGoogleBusinessAttributes200ResponseAttributesInner.new(
  name: null,
  value_type: null,
  values: null,
  repeated_enum_value: null
)
```

