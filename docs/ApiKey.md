# Late::ApiKey

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  | [optional] |
| **name** | **String** |  | [optional] |
| **key_preview** | **String** |  | [optional] |
| **expires_at** | **Time** |  | [optional] |
| **created_at** | **Time** |  | [optional] |
| **key** | **String** | Returned only once, on creation | [optional] |

## Example

```ruby
require 'late'

instance = Late::ApiKey.new(
  id: null,
  name: null,
  key_preview: null,
  expires_at: null,
  created_at: null,
  key: null
)
```

