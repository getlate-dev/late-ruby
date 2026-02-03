# Late::SelectLinkedInOrganization200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **message** | **String** |  | [optional] |
| **redirect_url** | **String** | The redirect URL with connection params appended (only if redirect_url was provided in request) | [optional] |
| **account** | [**SelectLinkedInOrganization200ResponseAccount**](SelectLinkedInOrganization200ResponseAccount.md) |  | [optional] |
| **bulk_refresh** | [**SelectLinkedInOrganization200ResponseBulkRefresh**](SelectLinkedInOrganization200ResponseBulkRefresh.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::SelectLinkedInOrganization200Response.new(
  message: null,
  redirect_url: null,
  account: null,
  bulk_refresh: null
)
```

