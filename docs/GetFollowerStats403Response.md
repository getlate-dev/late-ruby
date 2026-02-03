# Late::GetFollowerStats403Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **error** | **String** |  | [optional] |
| **message** | **String** |  | [optional] |
| **requires_addon** | **Boolean** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::GetFollowerStats403Response.new(
  error: Analytics add-on required,
  message: Follower stats tracking requires the Analytics add-on. Please upgrade to access this feature.,
  requires_addon: true
)
```

