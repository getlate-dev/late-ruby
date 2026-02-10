# Late::ConnectionLogContext

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **is_headless_mode** | **Boolean** |  | [optional] |
| **has_custom_redirect_url** | **Boolean** |  | [optional] |
| **is_reconnection** | **Boolean** |  | [optional] |
| **is_byok** | **Boolean** | Using bring-your-own-keys | [optional] |
| **invitation_token** | **String** |  | [optional] |
| **connect_token** | **String** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::ConnectionLogContext.new(
  is_headless_mode: null,
  has_custom_redirect_url: null,
  is_reconnection: null,
  is_byok: null,
  invitation_token: null,
  connect_token: null
)
```

