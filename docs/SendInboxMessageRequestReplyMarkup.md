# Late::SendInboxMessageRequestReplyMarkup

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Keyboard type | [optional] |
| **keyboard** | **Array&lt;Array&lt;SendInboxMessageRequestReplyMarkupKeyboardInnerInner&gt;&gt;** | Array of rows, each row is an array of buttons | [optional] |
| **one_time** | **Boolean** | Hide keyboard after use (reply_keyboard only) | [optional][default to true] |

## Example

```ruby
require 'late'

instance = Late::SendInboxMessageRequestReplyMarkup.new(
  type: null,
  keyboard: null,
  one_time: null
)
```

