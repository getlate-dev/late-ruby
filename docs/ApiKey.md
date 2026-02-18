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
| **scope** | **String** | &#39;full&#39; grants access to all profiles, &#39;profiles&#39; restricts to specific profiles | [optional][default to &#39;full&#39;] |
| **profile_ids** | [**Array&lt;ApiKeyProfileIdsInner&gt;**](ApiKeyProfileIdsInner.md) | Profiles this key can access (populated with name and color). Only present when scope is &#39;profiles&#39;. | [optional] |
| **permission** | **String** | &#39;read-write&#39; allows all operations, &#39;read&#39; restricts to GET requests only | [optional][default to &#39;read-write&#39;] |

## Example

```ruby
require 'late'

instance = Late::ApiKey.new(
  id: null,
  name: null,
  key_preview: null,
  expires_at: null,
  created_at: null,
  key: null,
  scope: null,
  profile_ids: null,
  permission: null
)
```

