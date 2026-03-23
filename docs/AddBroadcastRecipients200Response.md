# Late::AddBroadcastRecipients200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **success** | **Boolean** |  | [optional] |
| **added** | **Integer** | Number of recipients successfully added | [optional] |
| **skipped** | **Integer** | Number skipped (duplicates or missing channels) | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::AddBroadcastRecipients200Response.new(
  success: null,
  added: null,
  skipped: null
)
```

