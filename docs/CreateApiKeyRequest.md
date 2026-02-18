# Late::CreateApiKeyRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **expires_in** | **Integer** | Days until expiry | [optional] |
| **scope** | **String** | &#39;full&#39; grants access to all profiles (default), &#39;profiles&#39; restricts to specific profiles | [optional][default to &#39;full&#39;] |
| **profile_ids** | **Array&lt;String&gt;** | Profile IDs this key can access. Required when scope is &#39;profiles&#39;. | [optional] |
| **permission** | **String** | &#39;read-write&#39; allows all operations (default), &#39;read&#39; restricts to GET requests only | [optional][default to &#39;read-write&#39;] |

## Example

```ruby
require 'late'

instance = Late::CreateApiKeyRequest.new(
  name: null,
  expires_in: null,
  scope: null,
  profile_ids: null,
  permission: null
)
```

