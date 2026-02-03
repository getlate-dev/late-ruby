# Late::WebhookPayloadAccountConnectedAccount

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** | The account&#39;s unique identifier (same as used in /v1/accounts/{accountId}) | [optional] |
| **profile_id** | **String** | The profile&#39;s unique identifier this account belongs to | [optional] |
| **platform** | **String** |  | [optional] |
| **username** | **String** |  | [optional] |
| **display_name** | **String** |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::WebhookPayloadAccountConnectedAccount.new(
  account_id: null,
  profile_id: null,
  platform: null,
  username: null,
  display_name: null
)
```

