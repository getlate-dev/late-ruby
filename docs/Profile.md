# Late::Profile

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **_id** | **String** |  | [optional] |
| **user_id** | **String** |  | [optional] |
| **name** | **String** |  | [optional] |
| **description** | **String** |  | [optional] |
| **color** | **String** |  | [optional] |
| **is_default** | **Boolean** |  | [optional] |
| **is_over_limit** | **Boolean** | Only present when includeOverLimit&#x3D;true. Indicates if this profile exceeds the plan limit. | [optional] |
| **created_at** | **Time** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::Profile.new(
  _id: null,
  user_id: null,
  name: null,
  description: null,
  color: null,
  is_default: null,
  is_over_limit: null,
  created_at: null
)
```

