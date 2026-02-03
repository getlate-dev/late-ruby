# Late::SelectSnapchatProfile200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message** | **String** |  | [optional] |
| **redirect_url** | **String** | Redirect URL with connection params (if provided in request) | [optional] |
| **account** | [**SelectSnapchatProfile200ResponseAccount**](SelectSnapchatProfile200ResponseAccount.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::SelectSnapchatProfile200Response.new(
  message: null,
  redirect_url: null,
  account: null
)
```

