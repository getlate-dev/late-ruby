# Late::SelectGoogleBusinessLocationRequestUserProfile

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  | [optional] |
| **name** | **String** |  | [optional] |
| **refresh_token** | **String** | Google refresh token for long-lived access | [optional] |
| **token_expires_in** | **Integer** | Token expiration time in seconds | [optional] |
| **scope** | **String** | Granted OAuth scopes | [optional] |

## Example

```ruby
require 'late'

instance = Late::SelectGoogleBusinessLocationRequestUserProfile.new(
  id: null,
  name: null,
  refresh_token: null,
  token_expires_in: null,
  scope: null
)
```

