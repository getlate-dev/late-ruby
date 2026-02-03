# Late::Connected

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** |  | [optional] |
| **chat_id** | **String** |  | [optional] |
| **chat_title** | **String** |  | [optional] |
| **chat_type** | **String** |  | [optional] |
| **account** | [**ConnectedAccount**](ConnectedAccount.md) |  | [optional] |

## Example

```ruby
require 'late'

instance = Late::Connected.new(
  status: null,
  chat_id: null,
  chat_title: null,
  chat_type: null,
  account: null
)
```

