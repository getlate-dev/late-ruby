# Late::CreateApiKeyRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **expires_in** | **Integer** | Days until expiry | [optional] |

## Example

```ruby
require 'late'

instance = Late::CreateApiKeyRequest.new(
  name: null,
  expires_in: null
)
```

