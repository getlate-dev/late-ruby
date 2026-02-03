# Late::SelectFacebookPage200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message** | **String** |  | [optional] |
| **redirect_url** | **String** | Redirect URL if custom redirect_url was provided | [optional] |
| **account** | [**SelectFacebookPage200ResponseAccount**](SelectFacebookPage200ResponseAccount.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::SelectFacebookPage200Response.new(
  message: null,
  redirect_url: null,
  account: null
)
```

