# Late::ListInboxConversations200ResponseMetaFailedAccountsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  | [optional] |
| **account_username** | **String** |  | [optional] |
| **platform** | **String** |  | [optional] |
| **error** | **String** |  | [optional] |
| **code** | **String** | Error code if available | [optional] |
| **retry_after** | **Integer** | Seconds to wait before retry (rate limits) | [optional] |

## Example

```ruby
require 'late'

instance = Late::ListInboxConversations200ResponseMetaFailedAccountsInner.new(
  account_id: null,
  account_username: null,
  platform: null,
  error: null,
  code: null,
  retry_after: null
)
```

