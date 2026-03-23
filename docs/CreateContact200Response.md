# Late::CreateContact200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **success** | **Boolean** |  | [optional] |
| **contact** | [**CreateContact200ResponseContact**](CreateContact200ResponseContact.md) |  | [optional] |
| **channel** | [**CreateContact200ResponseChannel**](CreateContact200ResponseChannel.md) |  | [optional] |
| **warning** | **String** |  | [optional] |

## Example

```ruby
require 'late-sdk'

instance = Late::CreateContact200Response.new(
  success: null,
  contact: null,
  channel: null,
  warning: null
)
```

